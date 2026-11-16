# Issue

**Title:** Dockerfile

## Description

## Description
This PR adds a Dockerfile which allows for easy installation of all python dependencies, the pyscreener library, ADFR suite tools and choice of vina based docking software to a contained docker image. This allows for reproducible and straightforward installation / testing / usage of the pyscreener code. All pytest checks pass as well as `smoke-test` for all vina versions.

## Example / Current workflow
Creating a docker image containing the pyscreener library, its dependencies, ADFR suite tools and the vina docking software can be accomplished with `docker build -t pyscreener:vina --target vina .` however any of the vina base docking softwares can be specified instead.

## Bugfix / Desired workflow
n/a

## Questions
Installing `qvina` / `psovina` requires building from source which raises some pragma issues during compilation. If any light can be shed on solving these issues / clarifying if these issues then that would be invaluable feedback.

## Relevant issues
n/a

## checklist
No new tests added but all docker builds pass the associated python and docking smoke tests

## Status
Not 100% ready as seeking feedback on compilation of `qvina` and `psovina` docking tools from souce

## Task

Modify the repository so that the issue described above is resolved. The repository is checked out at base commit `71762e8b5ab8`. Edit files in place; the verifier captures your changes via `git diff` and scores them against an oracle patch using SWE-RL-style diff-similarity reward.