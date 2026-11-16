# Issue

**Title:** feat: add pacsomatic skill

## Description

Summary

This PR adds a new pacsomatic skill package aligned with K-DENSE skill conventions, including required structure, routing-focused SKILL documentation, baseline configuration, and unit tests.

Included

1. SKILL.md
2. config.yaml
3. run_pacsomatic.py
4. test_run_pacsomatic.py
5. agent-playbook.md
6. config-and-output.md
7. pacsomatic_guide.md
8. README.md
9. LICENSE

Notes

1. No functional break to the helper script behavior; this is mainly a packaging/documentation/test alignment update.
2. Skill routing guidance now clearly defines trigger phrases, dry-run vs run behavior, and expected agent response fields.

Validation

1. `python -m unittest discover -s tests -v`
2. Result: 7 tests passed

## Task

Modify the repository so that the issue described above is resolved. The repository is checked out at base commit `7a1d69cc3feb`. Edit files in place; the verifier captures your changes via `git diff` and scores them against an oracle patch using SWE-RL-style diff-similarity reward.