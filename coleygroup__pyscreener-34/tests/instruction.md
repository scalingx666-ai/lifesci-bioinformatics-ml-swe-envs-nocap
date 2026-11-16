# Issue

**Title:** fix coverage

## Description

## Description
finally fix the coverage

## Example / Current workflow
coverage doesn't work in the current actions

## Bugfix / Desired workflow
adding a `__init__.py` to the `test` folder fixes the problem and now displays coverage correctly

## checklist
- [x] (if appropriate) unit tests added: `pytest`

## Status
- [x] Ready to go

## Task

Modify the repository so that the issue described above is resolved. The repository is checked out at base commit `7c69f4463a71`. Edit files in place; the verifier captures your changes via `git diff` and scores them against an oracle patch using SWE-RL-style diff-similarity reward.