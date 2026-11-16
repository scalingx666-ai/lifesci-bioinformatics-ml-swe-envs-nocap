# Issue

**Title:** Fix e-value filtering + handle filenames with '.'

## Description

Hi,

When running `reseek -search` in sensitive mode I noticed that the hits were not being filtered on e-value (`-fast` mode was fine). I got hits with e-values above 10 and also when specifically setting `-evalue` nothing changed. I tracked it down to `DBSearcher::Reject` where both `Evalue_ok` and `TS_ok` should be `false` before any filtering happens, however if the `mints` option is not set, this never happens. I changed the logic and now return `true` if either of the evaluations is true.

I also took the liberty to update the `GetStemName` function so it can handle dots in filenames apart from the file extension (also ignoring .gz extensions).

Edit: I was using the latest released version of reseek v2.7.i86linux64 [35e1fa2]

## Task

Modify the repository so that the issue described above is resolved. The repository is checked out at base commit `e5bb2b6ec738`. Edit files in place; the verifier captures your changes via `git diff` and scores them against an oracle patch using SWE-RL-style diff-similarity reward.