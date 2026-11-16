# Issue

**Title:** Bump ray `1->2`

## Description

## Description
This PR bumps the ray version from 1 to 2

## The problem
Ray v2 has deprecated the `ray.state` module, so the calculation of the `node_id` attribute of the `Result` objects raises a `DeprecationWarning` and will likely break in the future

## The fix
This PR adds specifications for the ray version in the packing config and switches out the following calls:
```
- ray.state.get_current_node_id()
+ ray.util.get_node_ip_address()
```

## Questions
I'm not actually certain these give the _same_ information, but it's not that important. They just need to give _some_ identifying information about the node on which the files are located for file collection at the end.

## Status
- [x] Ready to go

## Task

Modify the repository so that the issue described above is resolved. The repository is checked out at base commit `084459a3d5af`. Edit files in place; the verifier captures your changes via `git diff` and scores them against an oracle patch using SWE-RL-style diff-similarity reward.