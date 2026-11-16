# Issue

**Title:** Upgrade GitHub Actions for Node 24 compatibility

## Description

## Summary

Upgrade GitHub Actions to their latest versions to ensure compatibility with Node 24, as Node 20 will reach end-of-life in April 2026.

## Changes

| Action | Old Version(s) | New Version | Release | Files |
|--------|---------------|-------------|---------|-------|
| `actions/checkout` | [`v4`](https://github.com/actions/checkout/releases/tag/v4) | [`v6`](https://github.com/actions/checkout/releases/tag/v6) | [Release](https://github.com/actions/checkout/releases/tag/v6) | release.yml |

## Context

Per [GitHub's announcement](https://github.blog/changelog/2025-09-19-deprecation-of-node-20-on-github-actions-runners/), Node 20 is being deprecated and runners will begin using Node 24 by default starting June 2nd, 2026.

### Why this matters

- **Node 20 EOL**: April 2026
- **Node 24 default**: June 2nd, 2026
- **Action**: Update to latest action versions that support Node 24

### ⚠️ Breaking Changes

- **actions/checkout** (v4 → v6): Major version upgrade — review the [release notes](https://github.com/actions/checkout/releases) for breaking changes

### Security Note

Actions that were previously pinned to commit SHAs remain pinned to SHAs (updated to the latest release SHA) to maintain the security benefits of immutable references.

### Testing

These changes only affect CI/CD workflow configurations and should not impact application functionality. The workflows should be tested by running them on a branch before merging.

## Task

Modify the repository so that the issue described above is resolved. The repository is checked out at base commit `b0923b2e06f7`. Edit files in place; the verifier captures your changes via `git diff` and scores them against an oracle patch using SWE-RL-style diff-similarity reward.