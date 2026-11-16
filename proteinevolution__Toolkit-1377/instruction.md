# Issue

**Title:** Update sbt-header to 5.6.5

## Description

Updates [de.heikoseeberger:sbt-header](https://github.com/sbt/sbt-header) from 5.6.0 to 5.6.5.
[GitHub Release Notes](https://github.com/sbt/sbt-header/releases/tag/v5.6.5) - [Version Diff](https://github.com/sbt/sbt-header/compare/v5.6.0...v5.6.5)

I'll automatically update this PR to resolve conflicts as long as you don't change it yourself.

If you'd like to skip this version, you can just close this PR. If you have any feedback, just mention me in the comments below.

Configure Scala Steward for your repository with a [`.scala-steward.conf`](https://github.com/scala-steward-org/scala-steward/blob/c1ea6ce89de1cd43e0e2858b97247725aec40f5d/docs/repo-specific-configuration.md) file.

Have a fantastic day writing Scala!

<details>
<summary>Files still referring to the old version number</summary>

The following files still refer to the old version number (5.6.0).
You might want to review and update them manually.
```
frontend/yarn.lock
```
</details>
<details>
<summary>Ignore future updates</summary>

Add this to your `.scala-steward.conf` file to ignore future updates of this dependency:
```
updates.ignore = [ { groupId = "de.heikoseeberger", artifactId = "sbt-header" } ]
```
</details>

labels: sbt-plugin-update, early-semver-patch, semver-spec-patch, old-version-remains, commit-count:1

## Task

Modify the repository so that the issue described above is resolved. The repository is checked out at base commit `169cf68d2341`. Edit files in place; the verifier captures your changes via `git diff` and scores them against an oracle patch using SWE-RL-style diff-similarity reward.