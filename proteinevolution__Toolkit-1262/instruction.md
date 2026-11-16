# Issue

**Title:** Update sbt-scalafmt to 2.4.3

## Description

Updates [org.scalameta:sbt-scalafmt](https://github.com/scalameta/sbt-scalafmt) from 2.4.2 to 2.4.3.
[GitHub Release Notes](https://github.com/scalameta/sbt-scalafmt/releases/tag/v2.4.3) - [Version Diff](https://github.com/scalameta/sbt-scalafmt/compare/v2.4.2...v2.4.3)

I'll automatically update this PR to resolve conflicts as long as you don't change it yourself.

If you'd like to skip this version, you can just close this PR. If you have any feedback, just mention me in the comments below.

Configure Scala Steward for your repository with a [`.scala-steward.conf`](https://github.com/scala-steward-org/scala-steward/blob/9d0aeb18896aef874382293d11317f4f313bfc7f/docs/repo-specific-configuration.md) file.

Have a fantastic day writing Scala!

<details>
<summary>Files still referring to the old version number</summary>

The following files still refer to the old version number (2.4.2).
You might want to review and update them manually.
```
frontend/yarn.lock
```
</details>
<details>
<summary>Ignore future updates</summary>

Add this to your `.scala-steward.conf` file to ignore future updates of this dependency:
```
updates.ignore = [ { groupId = "org.scalameta", artifactId = "sbt-scalafmt" } ]
```
</details>

labels: sbt-plugin-update, semver-patch, old-version-remains

## Task

Modify the repository so that the issue described above is resolved. The repository is checked out at base commit `f7779539ef7e`. Edit files in place; the verifier captures your changes via `git diff` and scores them against an oracle patch using SWE-RL-style diff-similarity reward.