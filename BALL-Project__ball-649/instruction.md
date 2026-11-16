# Issue

**Title:** Use GNUInstallDirs

## Description

Makes for some uncluttering and standards using, this way distributions can comfortably override `CMAKE_INSTALL_LIBDIR` for their multiarch layout and `CMAKE_INSTALL_DOCDIR` for their docdir naming defaults.

## Task

Modify the repository so that the issue described above is resolved. The repository is checked out at base commit `e80b5e2021a7`. Edit files in place; the verifier captures your changes via `git diff` and scores them against an oracle patch using SWE-RL-style diff-similarity reward.