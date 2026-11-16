# Issue

**Title:** Update scalafmt-core to 3.0.5

## Description

Updates [org.scalameta:scalafmt-core](https://github.com/scalameta/scalafmt) from 3.0.4 to 3.0.5.
[GitHub Release Notes](https://github.com/scalameta/scalafmt/releases/tag/v3.0.5) - [Version Diff](https://github.com/scalameta/scalafmt/compare/v3.0.4...v3.0.5)

I'll automatically update this PR to resolve conflicts as long as you don't change it yourself.

If you'd like to skip this version, you can just close this PR. If you have any feedback, just mention me in the comments below.

Configure Scala Steward for your repository with a [`.scala-steward.conf`](https://github.com/scala-steward-org/scala-steward/blob/89b198bf80f7d7139bcf1206897a3298c822d3a7/docs/repo-specific-configuration.md) file.

Have a fantastic day writing Scala!

<details>
<summary>Files still referring to the old version number</summary>

The following files still refer to the old version number (3.0.4).
You might want to review and update them manually.
```
frontend/yarn.lock
```
</details>
<details>
<summary>Ignore future updates</summary>

Add this to your `.scala-steward.conf` file to ignore future updates of this dependency:
```
updates.ignore = [ { groupId = "org.scalameta", artifactId = "scalafmt-core" } ]
```
</details>

labels: library-update, semver-patch, old-version-remains

## Task

Modify the repository so that the issue described above is resolved. The repository is checked out at base commit `1742bdfb326c`. Edit files in place; the verifier captures your changes via `git diff` and scores them against an oracle patch using SWE-RL-style diff-similarity reward.