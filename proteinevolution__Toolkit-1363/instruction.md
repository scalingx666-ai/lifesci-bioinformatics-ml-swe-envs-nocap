# Issue

**Title:** Update sbt-scoverage to 1.9.3

## Description

Updates [org.scoverage:sbt-scoverage](https://github.com/scoverage/sbt-scoverage) from 1.9.2 to 1.9.3.
[GitHub Release Notes](https://github.com/scoverage/sbt-scoverage/releases/tag/v1.9.3) - [Version Diff](https://github.com/scoverage/sbt-scoverage/compare/v1.9.2...v1.9.3)

I'll automatically update this PR to resolve conflicts as long as you don't change it yourself.

If you'd like to skip this version, you can just close this PR. If you have any feedback, just mention me in the comments below.

Configure Scala Steward for your repository with a [`.scala-steward.conf`](https://github.com/scala-steward-org/scala-steward/blob/1169d43f591dcde4f76088681e21627dcdf34f70/docs/repo-specific-configuration.md) file.

Have a fantastic day writing Scala!

<details>
<summary>Ignore future updates</summary>

Add this to your `.scala-steward.conf` file to ignore future updates of this dependency:
```
updates.ignore = [ { groupId = "org.scoverage", artifactId = "sbt-scoverage" } ]
```
</details>

labels: sbt-plugin-update, early-semver-patch, semver-spec-patch, commit-count:1

## Task

Modify the repository so that the issue described above is resolved. The repository is checked out at base commit `5960d3da79af`. Edit files in place; the verifier captures your changes via `git diff` and scores them against an oracle patch using SWE-RL-style diff-similarity reward.