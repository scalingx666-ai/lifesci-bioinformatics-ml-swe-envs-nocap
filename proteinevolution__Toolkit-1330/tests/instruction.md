# Issue

**Title:** Update cats-effect to 3.3.0

## Description

Updates [org.typelevel:cats-effect](https://github.com/typelevel/cats-effect) from 3.2.9 to 3.3.0.
[GitHub Release Notes](https://github.com/typelevel/cats-effect/releases/tag/v3.3.0) - [Version Diff](https://github.com/typelevel/cats-effect/compare/v3.2.9...v3.3.0)

I'll automatically update this PR to resolve conflicts as long as you don't change it yourself.

If you'd like to skip this version, you can just close this PR. If you have any feedback, just mention me in the comments below.

Configure Scala Steward for your repository with a [`.scala-steward.conf`](https://github.com/scala-steward-org/scala-steward/blob/0b3ab9ecc62b5fdc6868c8d8feaab0c31c803535/docs/repo-specific-configuration.md) file.

Have a fantastic day writing Scala!

<details>
<summary>Applied Scalafix Migrations</summary>

* org.typelevel:{cats-effect,cats-effect-laws}:3.3.0 (created no change)
  * github:typelevel/cats-effect/v3_3_0?sha=series/3.x
</details>
<details>
<summary>Ignore future updates</summary>

Add this to your `.scala-steward.conf` file to ignore future updates of this dependency:
```
updates.ignore = [ { groupId = "org.typelevel", artifactId = "cats-effect" } ]
```
</details>

labels: library-update, early-semver-minor, semver-spec-minor, scalafix-migrations

## Task

Modify the repository so that the issue described above is resolved. The repository is checked out at base commit `7eb17a803891`. Edit files in place; the verifier captures your changes via `git diff` and scores them against an oracle patch using SWE-RL-style diff-similarity reward.