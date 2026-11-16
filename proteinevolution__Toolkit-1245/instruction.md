# Issue

**Title:** Bump dns-packet from 1.3.1 to 1.3.4 in /frontend

## Description

Bumps [dns-packet](https://github.com/mafintosh/dns-packet) from 1.3.1 to 1.3.4.
<details>
<summary>Commits</summary>
<ul>
<li><a href=""><code>ebdf849</code></a> 1.3.4</li>
<li><a href=""><code>ac57872</code></a> move all allocUnsafes to allocs for easier maintenance</li>
<li><a href=""><code>c64c950</code></a> 1.3.3</li>
<li><a href=""><code>0598ba1</code></a> fix .. in encodingLength</li>
<li><a href=""><code>010aedb</code></a> 1.3.2</li>
<li><a href=""><code>0d0d593</code></a> backport encodingLength fix to v1</li>
<li>See full diff in <a href="https://github.com/mafintosh/dns-packet/compare/v1.3.1...v1.3.4">compare view</a></li>
</ul>
</details>
<br />

[![Dependabot compatibility score](https://dependabot-badges.githubapp.com/badges/compatibility_score?dependency-name=dns-packet&package-manager=npm_and_yarn&previous-version=1.3.1&new-version=1.3.4)](https://docs.github.com/en/github/managing-security-vulnerabilities/about-dependabot-security-updates#about-compatibility-scores)

Dependabot will resolve any conflicts with this PR as long as you don't alter it yourself. You can also trigger a rebase manually by commenting `@dependabot rebase`.

[//]: # (dependabot-automerge-start)
[//]: # (dependabot-automerge-end)

---

<details>
<summary>Dependabot commands and options</summary>
<br />

You can trigger Dependabot actions by commenting on this PR:
- `@dependabot rebase` will rebase this PR
- `@dependabot recreate` will recreate this PR, overwriting any edits that have been made to it
- `@dependabot merge` will merge this PR after your CI passes on it
- `@dependabot squash and merge` will squash and merge this PR after your CI passes on it
- `@dependabot cancel merge` will cancel a previously requested merge and block automerging
- `@dependabot reopen` will reopen this PR if it is closed
- `@dependabot close` will close this PR and stop Dependabot recreating it. You can achieve the same result by closing it manually
- `@dependabot ignore this major version` will close this PR and stop Dependabot creating any more for this major version (unless you reopen the PR or upgrade to it yourself)
- `@dependabot ignore this minor version` will close this PR and stop Dependabot creating any more for this minor version (unless you reopen the PR or upgrade to it yourself)
- `@dependabot ignore this dependency` will close this PR and stop Dependabot creating any more for this dependency (unless you reopen the PR or upgrade to it yourself)
- `@dependabot use these labels` will set the current labels as the default for future PRs for this repo and language
- `@dependabot use these reviewers` will set the current reviewers as the default for future PRs for this repo and language
- `@dependabot use these assignees` will set the current assignees as the default for future PRs for this repo and language
- `@dependabot use this milestone` will set the current milestone as the default for future PRs for this repo and language

You can disable automated security fix PRs for this repo from the [Security Alerts page](https://github.com/proteinevolution/Toolkit/network/alerts).

</details>

## Task

Modify the repository so that the issue described above is resolved. The repository is checked out at base commit `524fe29ed80c`. Edit files in place; the verifier captures your changes via `git diff` and scores them against an oracle patch using SWE-RL-style diff-similarity reward.