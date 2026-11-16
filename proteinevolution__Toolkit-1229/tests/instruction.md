# Issue

**Title:** Update cats-core to 2.6.1

## Description

Updates [org.typelevel:cats-core](https://github.com/typelevel/cats) from 2.6.0 to 2.6.1.
[GitHub Release Notes](https://github.com/typelevel/cats/releases/tag/v2.6.1) - [Changelog](https://github.com/typelevel/cats/blob/master/CHANGES.md) - [Version Diff](https://github.com/typelevel/cats/compare/v2.6.0...v2.6.1)

I'll automatically update this PR to resolve conflicts as long as you don't change it yourself.

If you'd like to skip this version, you can just close this PR. If you have any feedback, just mention me in the comments below.

Configure Scala Steward for your repository with a [`.scala-steward.conf`](https://github.com/scala-steward-org/scala-steward/blob/fafd3807343bf6a15e7c2ab8b12f01b84c1464ff/docs/repo-specific-configuration.md) file.

Have a fantastic day writing Scala!

<details>
<summary>Files still referring to the old version number</summary>

The following files still refer to the old version number (2.6.0).
You might want to review and update them manually.
```
frontend/yarn.lock
```
</details>
<details>
<summary>Ignore future updates</summary>

Add this to your `.scala-steward.conf` file to ignore future updates of this dependency:
```
updates.ignore = [ { groupId = "org.typelevel", artifactId = "cats-core" } ]
```
</details>

labels: library-update, semver-patch, old-version-remains

## Task

Modify the repository so that the issue described above is resolved. The repository is checked out at base commit `c0dfdcd281b8`. Edit files in place; the verifier captures your changes via `git diff` and scores them against an oracle patch using SWE-RL-style diff-similarity reward.