# Issue

**Title:** Update sbt-release to 1.1.0

## Description

Updates [com.github.sbt:sbt-release](https://github.com/sbt/sbt-release) from 1.0.15 to 1.1.0.
[GitHub Release Notes](https://github.com/sbt/sbt-release/releases/tag/v1.1.0) - [Version Diff](https://github.com/sbt/sbt-release/compare/v1.0.15...v1.1.0)

I'll automatically update this PR to resolve conflicts as long as you don't change it yourself.

If you'd like to skip this version, you can just close this PR. If you have any feedback, just mention me in the comments below.

Configure Scala Steward for your repository with a [`.scala-steward.conf`](https://github.com/scala-steward-org/scala-steward/blob/fcb3205568718165f2edd88599e603ee21886132/docs/repo-specific-configuration.md) file.

Have a fantastic day writing Scala!

<details>
<summary>Ignore future updates</summary>

Add this to your `.scala-steward.conf` file to ignore future updates of this dependency:
```
updates.ignore = [ { groupId = "com.github.sbt", artifactId = "sbt-release" } ]
```
</details>

labels: sbt-plugin-update, semver-minor

## Task

Modify the repository so that the issue described above is resolved. The repository is checked out at base commit `39f00546b894`. Edit files in place; the verifier captures your changes via `git diff` and scores them against an oracle patch using SWE-RL-style diff-similarity reward.