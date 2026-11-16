# Issue

**Title:** Feature/entry point scripts

## Description

## Description
adding command line entry point scripts to eliminate need for `run.py`

## Todos
Notable points that this PR has either accomplished or will accomplish.
  - [X] add two command line entry points: `pyscreener` and `pyscreener-check` to run pyscreener and check the environment for proper setup, respectively
  - [ ] remove the old `run.py` script and the `--smoke-test` arg

## Questions
- [ ] should we eliminate passing metadata as a string and require users to specify it as a JSON file?

## Status
- [X] Ready to go

## Task

Modify the repository so that the issue described above is resolved. The repository is checked out at base commit `993883eab385`. Edit files in place; the verifier captures your changes via `git diff` and scores them against an oracle patch using SWE-RL-style diff-similarity reward.