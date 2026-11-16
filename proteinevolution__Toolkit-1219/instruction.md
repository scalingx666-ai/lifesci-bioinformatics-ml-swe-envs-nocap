# Issue

**Title:** Update sbt-scoverage to 1.7.2

## Description

Updates [org.scoverage:sbt-scoverage](https://github.com/scoverage/sbt-scoverage) from 1.7.0 to 1.7.2.
[GitHub Release Notes](https://github.com/scoverage/sbt-scoverage/releases/tag/v1.7.2) - [Version Diff](https://github.com/scoverage/sbt-scoverage/compare/v1.7.0...v1.7.2)

I'll automatically update this PR to resolve conflicts as long as you don't change it yourself.

If you'd like to skip this version, you can just close this PR. If you have any feedback, just mention me in the comments below.

Configure Scala Steward for your repository with a [`.scala-steward.conf`](https://github.com/scala-steward-org/scala-steward/blob/49ad74410ad639b2623448cb9bff0afedab9aa3c/docs/repo-specific-configuration.md) file.

Have a fantastic day writing Scala!

<details>
<summary>Files still referring to the old version number</summary>

The following files still refer to the old version number (1.7.0).
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

labels: sbt-plugin-update, semver-patch, old-version-remains

## Task

Modify the repository so that the issue described above is resolved. The repository is checked out at base commit `32b6d2a973a5`. Edit files in place; the verifier captures your changes via `git diff` and scores them against an oracle patch using SWE-RL-style diff-similarity reward.