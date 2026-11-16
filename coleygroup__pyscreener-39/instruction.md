# Issue

**Title:** remove deprecated arguments

## Description

## Description
the `repeat_score_mode` and `repeat` arguments were deprecated in the last minor release, and this broke the CLI. this PR removes all traces of these deprecated variables/arguments

## Relevant issues
#38 

## checklist
- [x] (if appropriate) unit tests added: `pytest`

## Status
- [x] Ready to go

## Task

Modify the repository so that the issue described above is resolved. The repository is checked out at base commit `ed3637116842`. Edit files in place; the verifier captures your changes via `git diff` and scores them against an oracle patch using SWE-RL-style diff-similarity reward.