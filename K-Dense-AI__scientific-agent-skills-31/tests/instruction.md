# Issue

**Title:** Add patentsview api key for patent search api

## Description

Changes:

1. Add PatentsView API key for patent search API, the USPTO API key can't be used for patent search, need to apply API key from [PatentsView](https://patentsview.org/api-v01-information-page)
2. Revise sample snippet for syntax error, obsolete field name (search_patents)

## Task

Modify the repository so that the issue described above is resolved. The repository is checked out at base commit `a7221bb237df`. Edit files in place; the verifier captures your changes via `git diff` and scores them against an oracle patch using SWE-RL-style diff-similarity reward.