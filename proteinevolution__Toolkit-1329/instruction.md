# Issue

**Title:** Update cats-core to 2.7.0

## Description

Updates [org.typelevel:cats-core](https://github.com/typelevel/cats) from 2.6.1 to 2.7.0.
[GitHub Release Notes](https://github.com/typelevel/cats/releases/tag/v2.7.0) - [Changelog](https://github.com/typelevel/cats/blob/master/CHANGES.md) - [Version Diff](https://github.com/typelevel/cats/compare/v2.6.1...v2.7.0)

I'll automatically update this PR to resolve conflicts as long as you don't change it yourself.

If you'd like to skip this version, you can just close this PR. If you have any feedback, just mention me in the comments below.

Configure Scala Steward for your repository with a [`.scala-steward.conf`](https://github.com/scala-steward-org/scala-steward/blob/f10f15afbc5fa14f0bbfed33407d3686e0803e4b/docs/repo-specific-configuration.md) file.

Have a fantastic day writing Scala!

<details>
<summary>Files still referring to the old version number</summary>

The following files still refer to the old version number (2.6.1).
You might want to review and update them manually.
```
frontend/package.json
frontend/yarn.lock
project/Dependencies.scala
```
</details>
<details>
<summary>Ignore future updates</summary>

Add this to your `.scala-steward.conf` file to ignore future updates of this dependency:
```
updates.ignore = [ { groupId = "org.typelevel", artifactId = "cats-core" } ]
```
</details>

labels: library-update, early-semver-minor, semver-spec-minor, old-version-remains

## Task

Modify the repository so that the issue described above is resolved. The repository is checked out at base commit `38a09fefef67`. Edit files in place; the verifier captures your changes via `git diff` and scores them against an oracle patch using SWE-RL-style diff-similarity reward.