# Issue

**Title:** Sync citation-management skill with claude-scientific-writer updates

## Description

## Summary

Ports the citation management and verification enhancements from the `claude-scientific-writer` repo into this repo's `citation-management` skill, plus venue-templates cross-references into `literature-review` and `peer-review`. The citation changes correspond to claude-scientific-writer commits `4bede21` ("enhance citation policies and writing standards") and `93dff38` ("enhance citation management and verification processes").

## Changes

### `skills/citation-management/SKILL.md`
- **New Phase 2.5: Metadata Enrichment via Web Search (MANDATORY)** — after metadata extraction and before BibTeX formatting, scan for incomplete entries (missing volume, pages, number, DOI) and fill gaps via web search. Commands are adapted from the source repo's `parallel_web.py` to this repo's `parallel-cli` convention (parallel-web skill).
- **Citation Count Standards by Venue** — target counts per venue type (Nature/Science/Cell 35-50+, NeurIPS/ICML/ICLR/CVPR/ACL 30-45+, literature reviews/market research 40-65+, NEJM/Lancet/JAMA 30-45+), plus guidance against lazy citation over-repetition.
- **Mandatory Post-Writing Reference Checks** — verify no unresolved in-text citations, no unused bibliography entries, venue-level citation counts, and complete metadata before final compilation.
- Updated `validate_citations.py` usage docs for the new flags and updated troubleshooting guidance.

### `skills/citation-management/scripts/validate_citations.py`
- New `--venue` flag: enforce venue-specific citation count standards (nature, science, cell, neurips, icml, iclr, cvpr, acl, review, nejm, lancet, jama, etc.).
- New `--min-count` flag: enforce a custom minimum citation count.
- New `--manuscript` flag: parse a Markdown or LaTeX manuscript, extract cited keys (`\cite{...}` variants and Pandoc `@key` syntax), and report unresolved citations (cited but not in `.bib`) as errors and unused entries (in `.bib` but never cited) as warnings.
- Copied verbatim from the source repo (strict superset of the previous version; existing flags unchanged).

### `skills/citation-management/references/citation_validation.md`
- Rewrote "Issue 3: Incomplete Extraction" with a mandatory web-search workflow for filling missing metadata, adapted to `parallel-cli`.

### `skills/literature-review/SKILL.md` and `skills/peer-review/SKILL.md`
- Ported venue-templates cross-references from claude-scientific-writer: literature-review gains a "Venue-Specific Writing Styles" section pointing to the venue-templates style guides (`venue_writing_styles.md`, `nature_science_style.md`, `cell_press_style.md`, `medical_journal_styles.md`); peer-review gains a pointer to `reviewer_expectations.md` for calibrating review standards to the target venue. All referenced files exist in this repo's `skills/venue-templates/`.

## What was intentionally NOT ported
- The source repo's other recent changes were to its own `CLAUDE.md`/`WRITER.md` orchestration docs; the skill-relevant policy content from those docs is folded into `citation-management/SKILL.md` here.
- The shared writing skills otherwise have had no upstream changes since the last sync — their remaining diffs are this repo's intentional divergences (parallel-cli integration, frontmatter metadata, elsarticle templates in venue-templates), which are preserved.
- The source's narrative-prose-over-bullets standards, which this repo's `scientific-writing` skill already covers.

## Testing
- `python3 -c "import ast; ast.parse(...)"` — script parses cleanly.
- `validate_citations.py --help` — all new flags present.
- Functional test with a 2-entry `.bib` + Markdown manuscript: correctly detects an unresolved citation key (error), an unused bibliography entry (warning), and a citation count below the Nature venue standard (error).

🤖 Generated with [Claude Code](https://claude.com/claude-code)

## Task

Modify the repository so that the issue described above is resolved. The repository is checked out at base commit `c8c5f9dc5640`. Edit files in place; the verifier captures your changes via `git diff` and scores them against an oracle patch using SWE-RL-style diff-similarity reward.