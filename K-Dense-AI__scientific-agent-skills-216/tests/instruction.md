# Issue

**Title:** Add OpenPIV skill under skills/openpiv

## Description

Resubmitting the OpenPIV skill as requested in #134.

### Changes Made:
- Moved skill location to `skills/openpiv/` matching `upstream/main` directory layout.
- Formatted `metadata` frontmatter as a single-line JSON object (`metadata: {"version": "1.0", "skill-author": "OpenPIV Team"}`).
- Included required `metadata.version` (`"1.0"`).
- Comprehensive `description` explaining what the skill does and when to use it.
- Added supporting reference documentation (`references/advanced_algorithms.md`) and runner/analysis scripts (`scripts/`).

## Task

Modify the repository so that the issue described above is resolved. The repository is checked out at base commit `bf383691e2a1`. Edit files in place; the verifier captures your changes via `git diff` and scores them against an oracle patch using SWE-RL-style diff-similarity reward.