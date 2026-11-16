# Issue

**Title:** feat(skills): add onekgpd skill: individual-level queries over the 1000 Genomes variant dataset

## Description

# feat(skills): add `onekgpd` skill: individual-level queries over the 1000 Genomes variant dataset

## Summary

This PR adds **`onekgpd`**, an Agent Skill for querying the **1000 Genomes
Project** high-coverage cohort (3,202 whole-genome-sequenced individuals,
GRCh38) at the level of individual participants. It lets an agent answer
questions such as *which individuals carry variants matching given criteria in a
gene or region*, *which variants exist in (or are carried by) a named set of
individuals*, *which individuals are homozygous-reference at a position*, and
*how related are two named individuals* — with variants returned alongside 1000
Genomes allele frequencies, gnomAD v4.1 exome/genome AF, AlphaMissense scores,
and HGVSp annotations.

The skill is a faithful replica of the [OneKGPd MCP server](https://github.com/dnaerys/onekgpd-mcp), repackaged to the
[Agent Skills specification](https://agentskills.io/specification). It is split into an **online variant layer**
(real-time gRPC/TLS queries against the public Dnaerys variant store)
and a fully **offline metadata layer** (sample, sex, pedigree, and population
queries answered from a bundled data file with the Python standard library only -
no network, no credentials).

## What's Included

- **`SKILL.md`** (363 lines) — manifest with overview, scope, when-to-use,
  capability map, per-command usage, and design conventions, with progressive
  disclosure into `references/`.
- **`scripts/onekgpd_api.py`** — online layer. Wraps the
  [Dnaerys Python Client](https://dnaerys-python.readthedocs.io/en/latest/) to
  query `db.dnaerys.org:443` over gRPC/TLS; owns the connection, server-side
  streaming, pagination, bounded retries, and JSON serialization. Ten
  subcommands. Its single dependency (`dnaerys`) is declared inline via
  [PEP 723](https://peps.python.org/pep-0723/), so `uv run` provisions it with no
  manual install.
- **`scripts/onekgpd_meta.py`** — offline layer. Standard-library only; reads the
  bundled data asset and reproduces the server's metadata semantics. Six
  subcommands.
- **`references/onekgpd_commands.md`** — full per-command argument tables and the
  output schema.
- **`references/annotation_vocabularies.md`** — controlled vocabularies for the
  CSV filter flags (VEP consequences/biotypes/impact, ClinVar significance,
  AlphaMissense classes, etc.).
- **`assets/kgpe.json`** — bundled pedigree/population data, plain JSON, 3,202
  records (~1 MB). No compressed or binary blobs; fully inspectable.

## Scientific Workflows Covered

- **Variant discovery in a region** — count then select variants in a GRCh38
  window in individuals or cohort-wide, filtered by allele frequency, predicted
  consequence, ClinVar clinical significance, gnomAD frequencies, AlphaMissense
  score/class and more - see annotation_vocabularies.md.
- **Cohort carrier identification** — find the individuals carrying variants that
  match given criteria in a region (`select-samples`), and the variants carried
  within a named subset of individuals (`*-in-samples`).
- **Homozygous-reference genotyping** — count/select individuals homozygous for
  the reference allele at a single position.
- **Relatedness / kinship** — relatedness degree and KING coefficient between two
  named individuals.
- **Population & pedigree metadata (offline)** — per-sample family, gender,
  parents, children, population, superpopulation, and phase3 status; population
  and superpopulation rosters with counts; per-population sex split, phase3, and
  trio membership; and selection of sample IDs by population/superpopulation
  across the 26 populations and 5 superpopulations (AFR, AMR, EAS, EUR, SAS).

A cohort selected by the offline metadata layer (e.g. all YRI individuals) can be
fed directly into the online variant layer, since sample IDs are shared across
both.

## Integration Points

- **Data source** — public Dnaerys variant store at `db.dnaerys.org:443`
  (gRPC/TLS), exposing 1000 Genomes 30x GRCh38 data sequenced/aligned by the New
  York Genome Center. Variants annotated with VEP 115 / GENCODE 49, ClinVar
  (202502), gnomAD v4.1, and AlphaMissense.
- **Runtime** — [`uv`](https://docs.astral.sh/uv/) is the only prerequisite; each
  script declares its dependencies inline (PEP 723). The offline layer has zero
  third-party dependencies.
- **Network** — only the online layer reaches the network (outbound TLS to the
  query endpoint). The offline metadata layer never touches the network.
- **No credentials** — no API keys, no `.env`, no environment variables, no
  `required_environment_variables`. Public, read-only dataset access.

## Files Layout

```text
skills/
└── onekgpd/
    ├── SKILL.md
    ├── scripts/
    │   ├── onekgpd_api.py              # online variant/sample/kinship queries (Dnaerys client)
    │   └── onekgpd_meta.py             # offline sample & population metadata (stdlib only)
    ├── references/
    │   ├── onekgpd_commands.md         # per-command argument tables + output schema
    │   └── annotation_vocabularies.md  # controlled vocabularies for the CSV filter flags
    └── assets/
        └── kgpe.json                   # bundled pedigree/population data (3,202 records)
```

## Scanner Results

Scanned with the Cisco AI skill scanner (behavioral analysis enabled):

```bash
skill-scanner scan ./skills/onekgpd --use-behavioral
```

- **Status: SAFE — 0 findings** (`max_severity: SAFE`, `findings_count: 0`).
- Analyzers run: `static_analyzer`, `bytecode`, `pipeline`, `behavioral_analyzer`.
- Policy: `default` (preset base `balanced`), policy version `1.0`.

The bundled asset is plain JSON (not a compressed archive or binary), so it is
fully analyzable and raises no archive/binary/low-analyzability findings.

## Validation

- **Frontmatter** — valid YAML. `name: onekgpd` matches the skill directory name;
  `description` is present and explains both what the skill does and when to use
  it; `metadata` is a **single-line JSON object** with a quoted
  `version: "1.0"` (per `CONTRIBUTING.md`, the form OpenClaw's line-based reader
  parses); `license: MIT` and a `compatibility` string declaring the Python
  requirement and the offline/online split are also set.
- **`SKILL.md` length** — 363 lines, within the spec's recommended ≤500, with
  longer material deferred to `references/`.
- **Cross-references** — every file referenced from `SKILL.md`
  (`scripts/onekgpd_api.py`, `scripts/onekgpd_meta.py`,
  `references/onekgpd_commands.md`, `references/annotation_vocabularies.md`,
  `assets/kgpe.json`) exists.
- **Scripts compile** — both pass `python -m py_compile`:

  ```bash
  python -m py_compile skills/onekgpd/scripts/onekgpd_api.py \
                       skills/onekgpd/scripts/onekgpd_meta.py
  ```

- **Security scan** — Cisco AI skill scanner: SAFE / 0 findings (see above).
- **Behavioral testing** — the skill is covered by a black-box test suite in the
  source repository that drives each script as a subprocess (`uv run …`) and
  asserts on exit code, stdout, stderr, and the JSON output file. The offline
  tier (metadata + CLI-contract, 34 tests) is fully deterministic and passes; a
  live tier exercises all online commands against the public endpoint and
  auto-skips when it is unreachable.
  [Test sources](https://github.com/dnaerys/onekgpd-skill/tree/master/tests).

## Licensing

- **Skill code:** MIT (declared in `SKILL.md` frontmatter; matches the source
  project's license).
- **Data:** the 1000 Genomes Project data is openly available for research use;
  the bundled `kgpe.json` contains only public pedigree/population metadata
  (sample IDs, family/parent IDs, sex, population, superpopulation, phase3
  indicator) — no private or unpublished data.

## Checklist

- [x] Adheres to the Agent Skills specification.
- [x] Skill directory name and `name` frontmatter match exactly (`onekgpd`).
- [x] `SKILL.md` has valid YAML frontmatter and a Markdown body with overview,
      when-to-use, capabilities, and concrete workflows/commands.
- [x] `metadata` is a single-line JSON object with a quoted `version`.
- [x] `SKILL.md` is concise (363 lines), with long material in `references/`.
- [x] All cross-referenced files exist.
- [x] Both scripts pass `python -m py_compile`.
- [x] Cisco AI skill scanner: SAFE / 0 findings.
- [x] No secrets, API keys, environment variables, or private data; no
      `required_environment_variables` needed.
- [x] References to official documentation included (Dnaerys client, dataset
      collection, annotation composition, PEP 723, `uv`).
- [x] Examples and commands have been tested.

## Task

Modify the repository so that the issue described above is resolved. The repository is checked out at base commit `75b944c18964`. Edit files in place; the verifier captures your changes via `git diff` and scores them against an oracle patch using SWE-RL-style diff-similarity reward.