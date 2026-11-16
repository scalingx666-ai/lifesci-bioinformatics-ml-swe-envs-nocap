# Issue

**Title:** Update cats-effect to 3.2.8

## Description

Updates [org.typelevel:cats-effect](https://github.com/typelevel/cats-effect) from 3.2.7 to 3.2.8.
[GitHub Release Notes](https://github.com/typelevel/cats-effect/releases/tag/v3.2.8) - [Version Diff](https://github.com/typelevel/cats-effect/compare/v3.2.7...v3.2.8)

I'll automatically update this PR to resolve conflicts as long as you don't change it yourself.

If you'd like to skip this version, you can just close this PR. If you have any feedback, just mention me in the comments below.

Configure Scala Steward for your repository with a [`.scala-steward.conf`](https://github.com/scala-steward-org/scala-steward/blob/b3bd1feecde963e31d7f4b546078fd34e32cb6f1/docs/repo-specific-configuration.md) file.

Have a fantastic day writing Scala!

<details>
<summary>Files still referring to the old version number</summary>

The following files still refer to the old version number (3.2.7).
You might want to review and update them manually.
```
frontend/yarn.lock
```
</details>
<details>
<summary>Ignore future updates</summary>

Add this to your `.scala-steward.conf` file to ignore future updates of this dependency:
```
updates.ignore = [ { groupId = "org.typelevel", artifactId = "cats-effect" } ]
```
</details>

labels: library-update, semver-patch, old-version-remains

## Task

Modify the repository so that the issue described above is resolved. The repository is checked out at base commit `04448cc02c6c`. Edit files in place; the verifier captures your changes via `git diff` and scores them against an oracle patch using SWE-RL-style diff-similarity reward.