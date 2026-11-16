# Issue

**Title:** Close two gaps in the skill link contract, and fix what they surface

## Description

# Summary

`link_problems` already checks that every `assets/`, `references/`, and `scripts/` path in a skill's docs resolves, but two gaps let broken references through anyway: it never scanned `assets/*.md`, and it only matched backticked or markdown-link spellings, so a bare `python scripts/thumbnail.py` inside a fenced block was invisible. A third gap sat in the meta suite, which applied every rule to script-bearing skills only — leaving 58 doc-only skills with their documents checked by nothing. This closes all three and fixes the eight real broken references they surface.

## Type of change

- [x] Update to an existing skill
- [x] Tests
- [x] Documentation

## Skills touched

- nextflow
- research-grants
- scientific-critical-thinking
- scientific-slides

## How this was tested

```
$ uv run skills-ref validate ./skills/{nextflow,research-grants,scientific-critical-thinking,scientific-slides}
Valid skill: skills/nextflow
Valid skill: skills/research-grants
Valid skill: skills/scientific-critical-thinking
Valid skill: skills/scientific-slides

$ uv run --with pytest python -m pytest tests/_meta -q
10 passed, 1492 subtests passed          # 1202 before: +290 from doc-only skills

$ uv run --with pytest --with pillow python -m pytest tests/scientific-slides -q
99 passed, 20 skipped, 103 subtests passed
```

`link_problems` reports 0 across all 162 skills after these fixes; it reported 2 before, both of which are fixed here.

The new coverage was verified negatively as well — a deliberately broken link in a doc-only skill and a deliberately broken command path in an `assets/` document each fail the suite, and neither would have been caught on `main`:

```
'research-grants: README.md:290 references `references/does_not_exist_xyz.md`, which does not exist'
'scientific-slides: powerpoint_design_guide.md:671 references `scripts/nonexistent_abc.py`, which does not exist'
```

## Related issues and references

None. Found by auditing in-repo path references across `skills/`.

---

## Checklist

**Skill format**

- [x] The skill directory name and the `name` frontmatter match exactly.
- [x] The skill directory contains only `SKILL.md`, `references/`, `scripts/`, and `assets/`.
- [x] `SKILL.md` has valid YAML frontmatter and a Markdown body.
- [x] Only the six spec-defined top-level fields are present.
- [x] `metadata` is a block mapping, not single-line JSON.
- [ ] Any `metadata.openclaw` or `metadata.hermes` block is a nested mapping — not touched by this PR; unchanged in all four skills.
- [x] `metadata.version` exists, is quoted, and is bumped: nextflow 1.1→1.2, research-grants 1.2→1.3, scientific-critical-thinking 1.2→1.3, scientific-slides 1.7→1.8.
- [ ] The `description` says both what the skill does and when an agent should use it — descriptions are unchanged by this PR.

**Validation and tests**

- [x] `uv run skills-ref validate ./skills/<name>` passes for all four.
- [ ] Tests live in `tests/<skill-name>/` — no new scripts ship here, so no new suite or `skill-requirements.toml` entry is needed.
- [x] Relevant test suites pass.
- [ ] Security scanner results — **not run**; the scanner needs `SKILL_SCANNER_LLM_API_KEY`, which I don't have. This PR adds no scripts and no executable content, only markdown and test code.

**Content and safety**

- [x] Examples were tested: every command path in the changed docs now resolves to a file that exists.
- [x] No secrets, credentials, private data, or unsafe instructions.
- [x] Credentials are named in `compatibility` — both skills carrying the schematic command already declare `OPENROUTER_API_KEY` there.
- [x] Relevant documentation is linked where useful.

## Notes for reviewers

**The narrow match on command paths is deliberate.** `_COMMAND_PATH` matches only the *executable* slot (`python …`, `bash …`, `./…`). Matching bare paths anywhere would flag three legitimate patterns that exist in the repo today: output paths (`generate-image` writes `-o assets/logo.svg`), incident records naming files that were *deliberately deleted* (`peer-review/references/security_validation.md`), and directory-tree illustrations (`pi-agent/references/skills.md`). None is a defect and none is flagged.

**The cross-skill rule is untouched and doing real work.** `bulk-rnaseq` → `pathway-enrichment`'s `scripts/run_enrichment.py` and `citation-management` → `pyzotero`'s `references/exports.md` both still resolve via the same-line owner rule.

**`DOCUMENT_RULES` is the judgement call worth a look.** I split the rules by what they read rather than adding a second registry: `frontmatter`, `skill_md_length`, `no_tests_under_skills`, `local_links_resolve`, and `no_personal_paths` read only documents and now run against every skill; the rest still run against script-bearing skills only. Applying them repo-wide surfaced zero additional failures beyond the ones fixed here, so this expands coverage without a backlog.

**scientific-slides needed more than a path correction.** Its PowerPoint guide documented a workflow built on `rearrange.py`, `inventory.py`, and `replace.py` — three scripts that exist in no skill in this repository — and pointed at `html2pptx.md` and `ooxml.md`, which the `pptx` skill no longer ships. I rewrote those sections against the skill as it actually is today (PptxGenJS for creation, unzip/edit/zip for templates, `thumbnail.py`/`add_slide.py`/`clean.py`/`office/validate.py`), rather than only repointing the paths.

## Task

Modify the repository so that the issue described above is resolved. The repository is checked out at base commit `1e5eeffbdad3`. Edit files in place; the verifier captures your changes via `git diff` and scores them against an oracle patch using SWE-RL-style diff-similarity reward.