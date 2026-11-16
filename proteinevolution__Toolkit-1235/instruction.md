# Issue

**Title:** Update shapeless to 2.3.7

## Description

Updates [com.chuusai:shapeless](https://github.com/milessabin/shapeless) from 2.3.6 to 2.3.7.
[GitHub Release Notes](https://github.com/milessabin/shapeless/releases/tag/v2.3.7) - [Version Diff](https://github.com/milessabin/shapeless/compare/v2.3.6...v2.3.7)

I'll automatically update this PR to resolve conflicts as long as you don't change it yourself.

If you'd like to skip this version, you can just close this PR. If you have any feedback, just mention me in the comments below.

Configure Scala Steward for your repository with a [`.scala-steward.conf`](https://github.com/scala-steward-org/scala-steward/blob/9b1175210c902dbb63ea03d1a2136868ffb54f16/docs/repo-specific-configuration.md) file.

Have a fantastic day writing Scala!

<details>
<summary>Files still referring to the old version number</summary>

The following files still refer to the old version number (2.3.6).
You might want to review and update them manually.
```
frontend/yarn.lock
```
</details>
<details>
<summary>Ignore future updates</summary>

Add this to your `.scala-steward.conf` file to ignore future updates of this dependency:
```
updates.ignore = [ { groupId = "com.chuusai", artifactId = "shapeless" } ]
```
</details>

labels: library-update, semver-patch, old-version-remains

## Task

Modify the repository so that the issue described above is resolved. The repository is checked out at base commit `0c302f241427`. Edit files in place; the verifier captures your changes via `git diff` and scores them against an oracle patch using SWE-RL-style diff-similarity reward.