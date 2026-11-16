# Issue

**Title:** Update scalafmt-core to 3.0.6

## Description

Updates [org.scalameta:scalafmt-core](https://github.com/scalameta/scalafmt) from 3.0.5 to 3.0.6.
[GitHub Release Notes](https://github.com/scalameta/scalafmt/releases/tag/v3.0.6) - [Version Diff](https://github.com/scalameta/scalafmt/compare/v3.0.5...v3.0.6)

I'll automatically update this PR to resolve conflicts as long as you don't change it yourself.

If you'd like to skip this version, you can just close this PR. If you have any feedback, just mention me in the comments below.

Configure Scala Steward for your repository with a [`.scala-steward.conf`](https://github.com/scala-steward-org/scala-steward/blob/6472b97b3365f2800f4202d1bf6b1d647bd2b0cc/docs/repo-specific-configuration.md) file.

Have a fantastic day writing Scala!

<details>
<summary>Ignore future updates</summary>

Add this to your `.scala-steward.conf` file to ignore future updates of this dependency:
```
updates.ignore = [ { groupId = "org.scalameta", artifactId = "scalafmt-core" } ]
```
</details>

labels: library-update, semver-patch

## Task

Modify the repository so that the issue described above is resolved. The repository is checked out at base commit `121f79f5e603`. Edit files in place; the verifier captures your changes via `git diff` and scores them against an oracle patch using SWE-RL-style diff-similarity reward.