# Issue

**Title:** Update sbt-scoverage to 1.9.0

## Description

Updates [org.scoverage:sbt-scoverage](https://github.com/scoverage/sbt-scoverage) from 1.8.2 to 1.9.0.
[GitHub Release Notes](https://github.com/scoverage/sbt-scoverage/releases/tag/v1.9.0) - [Version Diff](https://github.com/scoverage/sbt-scoverage/compare/v1.8.2...v1.9.0)

I'll automatically update this PR to resolve conflicts as long as you don't change it yourself.

If you'd like to skip this version, you can just close this PR. If you have any feedback, just mention me in the comments below.

Configure Scala Steward for your repository with a [`.scala-steward.conf`](https://github.com/scala-steward-org/scala-steward/blob/8d147634d322f0cc7208b401542428a7d02d51c6/docs/repo-specific-configuration.md) file.

Have a fantastic day writing Scala!

<details>
<summary>Files still referring to the old version number</summary>

The following files still refer to the old version number (1.8.2).
You might want to review and update them manually.
```
frontend/yarn.lock
```
</details>
<details>
<summary>Ignore future updates</summary>

Add this to your `.scala-steward.conf` file to ignore future updates of this dependency:
```
updates.ignore = [ { groupId = "org.scoverage", artifactId = "sbt-scoverage" } ]
```
</details>

labels: sbt-plugin-update, semver-minor, old-version-remains

## Task

Modify the repository so that the issue described above is resolved. The repository is checked out at base commit `e83a1384f439`. Edit files in place; the verifier captures your changes via `git diff` and scores them against an oracle patch using SWE-RL-style diff-similarity reward.