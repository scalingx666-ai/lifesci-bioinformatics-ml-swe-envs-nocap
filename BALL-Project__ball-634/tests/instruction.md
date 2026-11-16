# Issue

**Title:** Revamped the workflow_support section

## Description

These new features were added:

- Support for CWL: A new version of CTDConverter including CWL support was released. Included this version in the CMake scripts.
- Added a `common` folder for generic tasks related to workflow support, such as installing miniconda, CTDConverter, etc.

Of course, code related to `ballaxy` was also modified to benefit from this new CTDConverter version and the new structure.

## Task

Modify the repository so that the issue described above is resolved. The repository is checked out at base commit `990aa0c06bf9`. Edit files in place; the verifier captures your changes via `git diff` and scores them against an oracle patch using SWE-RL-style diff-similarity reward.