# Issue

**Title:** Improve build logic

## Description

(*) vcxproj2makefile_linux.py deleted, idea is build_linux/win should do everything.
(*) build_linux.py:
- error if uncommitted changes
- generates gitver.txt
- generates Makefile
- deletes o/myutils.o and ../bin/reseek to force re-build (myutils.cpp #include's gitver.txt)
- runs make
(*) build_win.py:
- error if uncommitted changes
- generates gitver.txt
- runs MSbuild

## Task

Modify the repository so that the issue described above is resolved. The repository is checked out at base commit `d7e98ed7dda0`. Edit files in place; the verifier captures your changes via `git diff` and scores them against an oracle patch using SWE-RL-style diff-similarity reward.