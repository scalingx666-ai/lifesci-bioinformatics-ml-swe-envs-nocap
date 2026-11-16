# Issue

**Title:** Update shapeless to 2.3.6

## Description

Updates [com.chuusai:shapeless](https://github.com/milessabin/shapeless) from 2.3.5 to 2.3.6.
[GitHub Release Notes](https://github.com/milessabin/shapeless/releases/tag/v2.3.6) - [Version Diff](https://github.com/milessabin/shapeless/compare/v2.3.5...v2.3.6)

I'll automatically update this PR to resolve conflicts as long as you don't change it yourself.

If you'd like to skip this version, you can just close this PR. If you have any feedback, just mention me in the comments below.

Configure Scala Steward for your repository with a [`.scala-steward.conf`](https://github.com/scala-steward-org/scala-steward/blob/ee8c7e989ffa9e9eccd9822d752f1459025dcb7b/docs/repo-specific-configuration.md) file.

Have a fantastic day writing Scala!

<details>
<summary>Files still referring to the old version number</summary>

The following files still refer to the old version number (2.3.5).
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

Modify the repository so that the issue described above is resolved. The repository is checked out at base commit `b3a1cccf8cff`. Edit files in place; the verifier captures your changes via `git diff` and scores them against an oracle patch using SWE-RL-style diff-similarity reward.