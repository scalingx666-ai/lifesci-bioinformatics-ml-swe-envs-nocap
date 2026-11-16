# Issue

**Title:** Update cats-effect to 3.2.3

## Description

Updates [org.typelevel:cats-effect](https://github.com/typelevel/cats-effect) from 3.2.2 to 3.2.3.
[GitHub Release Notes](https://github.com/typelevel/cats-effect/releases/tag/v3.2.3) - [Version Diff](https://github.com/typelevel/cats-effect/compare/v3.2.2...v3.2.3)

I'll automatically update this PR to resolve conflicts as long as you don't change it yourself.

If you'd like to skip this version, you can just close this PR. If you have any feedback, just mention me in the comments below.

Configure Scala Steward for your repository with a [`.scala-steward.conf`](https://github.com/scala-steward-org/scala-steward/blob/9e571d74f5c3f19687a5cd5c2283576d33b31daf/docs/repo-specific-configuration.md) file.

Have a fantastic day writing Scala!

<details>
<summary>Files still referring to the old version number</summary>

The following files still refer to the old version number (3.2.2).
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

Modify the repository so that the issue described above is resolved. The repository is checked out at base commit `8c9c6b6142c8`. Edit files in place; the verifier captures your changes via `git diff` and scores them against an oracle patch using SWE-RL-style diff-similarity reward.