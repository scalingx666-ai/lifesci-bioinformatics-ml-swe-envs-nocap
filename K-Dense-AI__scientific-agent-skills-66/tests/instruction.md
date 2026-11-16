# Issue

**Title:** Add parallel-web skill and update research-lookup

## Description

## Summary

- **parallel-web**: New skill for web search, deep research, and URL extraction via Parallel Chat API and Extract API
- **research-lookup**: Updated to latest version from claude-scientific-writer with dual-backend routing (Parallel Chat API primary, Perplexity for academic paper searches)

Both skills use frontmatter format consistent with other skills in the collection.

Made with [Cursor](https://cursor.com)

## Task

Modify the repository so that the issue described above is resolved. The repository is checked out at base commit `29c869326e92`. Edit files in place; the verifier captures your changes via `git diff` and scores them against an oracle patch using SWE-RL-style diff-similarity reward.