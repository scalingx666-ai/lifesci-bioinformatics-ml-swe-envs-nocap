# Issue

**Title:** Bump browserslist from 4.16.4 to 4.16.6 in /frontend

## Description

Bumps [browserslist](https://github.com/browserslist/browserslist) from 4.16.4 to 4.16.6.
<details>
<summary>Changelog</summary>
<p><em>Sourced from <a href="https://github.com/browserslist/browserslist/blob/main/CHANGELOG.md">browserslist's changelog</a>.</em></p>
<blockquote>
<h2>4.16.6</h2>
<ul>
<li>Fixed <code>npm-shrinkwrap.json</code> support in <code>--update-db</code> (by Geoff Newman).</li>
</ul>
<h2>4.16.5</h2>
<ul>
<li>Fixed unsafe RegExp (by Yeting Li).</li>
</ul>
</blockquote>
</details>
<details>
<summary>Commits</summary>
<ul>
<li><a href=""><code>6fe3614</code></a> Release 4.16.6 version</li>
<li><a href=""><code>33ebac9</code></a> Update dependencies</li>
<li><a href=""><code>2128170</code></a> Add support for npm-shrinkwrap files alongside package-lock (<a href="https://github-redirect.dependabot.com/browserslist/browserslist/issues/595">#595</a>)</li>
<li><a href=""><code>7cc2aed</code></a> Release 4.16.5 version</li>
<li><a href=""><code>27e4afd</code></a> Update dependencies</li>
<li><a href=""><code>1013a18</code></a> Fix version RegExp</li>
<li><a href=""><code>b879a1a</code></a> Use Node.js 16 on CI</li>
<li><a href=""><code>bd1e9e0</code></a> Fix ReDoS (<a href="https://github-redirect.dependabot.com/browserslist/browserslist/issues/593">#593</a>)</li>
<li>See full diff in <a href="https://github.com/browserslist/browserslist/compare/4.16.4...4.16.6">compare view</a></li>
</ul>
</details>
<br />

[![Dependabot compatibility score](https://dependabot-badges.githubapp.com/badges/compatibility_score?dependency-name=browserslist&package-manager=npm_and_yarn&previous-version=4.16.4&new-version=4.16.6)](https://docs.github.com/en/github/managing-security-vulnerabilities/about-dependabot-security-updates#about-compatibility-scores)

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

Modify the repository so that the issue described above is resolved. The repository is checked out at base commit `eab282e5e95e`. Edit files in place; the verifier captures your changes via `git diff` and scores them against an oracle patch using SWE-RL-style diff-similarity reward.