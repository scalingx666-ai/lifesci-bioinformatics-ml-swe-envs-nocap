# Issue

**Title:** Multi lines

## Description

Refactor of how `m_add_lines()` is handled along the lines of this thread: #15 


- `m_add_line()` changed to `.m_add_line()` and now only used internally
- `m_add_lines()` is now the primary line addition function. 
  - arguments are: `starts` and `ends` which can take either a single `m_sel()` selection or a list of selections such as `list(m_sel(), m_sel())`
  - If `length(ends) == length(starts)` then a line is drawn between each pair of selections
  - if `length(ends) != length(starts)` or `pairwise == TRUE` then a line is drawn between every combination of `starts` and `ends`.
  - Lines are added by calling the `.m_add_line()` internal function
- Addition of `m_multiresi_sel()` which can be used for creating multiple residue selections quickly. 
  - `m_sel(resi = 1:10)` will create 1 selection that contains all 10 residues. 
  - `m_multiresi_sel(1:10)` will create 10 different selections, each containing one of the residues specified.
  - Useful for passing into `m_add_lines()`

Any comments on the structure of it all welcomed. If it's all looking good I'll go through and apply the same principle to the other `m_add_*` functions.

## Task

Modify the repository so that the issue described above is resolved. The repository is checked out at base commit `93aea9f6b45d`. Edit files in place; the verifier captures your changes via `git diff` and scores them against an oracle patch using SWE-RL-style diff-similarity reward.