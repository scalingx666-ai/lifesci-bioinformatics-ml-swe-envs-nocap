# Issue

**Title:** Update circe-generic, ... to 0.14.1

## Description

Updates
* [io.circe:circe-generic](https://github.com/circe/circe)
* [io.circe:circe-generic-extras](https://github.com/circe/circe-generic-extras)

 from 0.13.0 to 0.14.1.
[GitHub Release Notes](https://github.com/circe/circe/releases/tag/v0.14.1) - [Version Diff](https://github.com/circe/circe/compare/v0.13.0...v0.14.1)

I'll automatically update this PR to resolve conflicts as long as you don't change it yourself.

If you'd like to skip this version, you can just close this PR. If you have any feedback, just mention me in the comments below.

Configure Scala Steward for your repository with a [`.scala-steward.conf`](https://github.com/scala-steward-org/scala-steward/blob/b73c3f0377d25faff4ce3b258e904abc7c607667/docs/repo-specific-configuration.md) file.

Have a fantastic day writing Scala!

<details>
<summary>Files still referring to the old version number</summary>

The following files still refer to the old version number (0.13.0).
You might want to review and update them manually.
```
build.sbt
```
</details>
<details>
<summary>Ignore future updates</summary>

Add this to your `.scala-steward.conf` file to ignore future updates of this dependency:
```
updates.ignore = [ { groupId = "io.circe" } ]
```
</details>

labels: library-update, semver-minor, old-version-remains

## Task

Modify the repository so that the issue described above is resolved. The repository is checked out at base commit `07ee1cc26a03`. Edit files in place; the verifier captures your changes via `git diff` and scores them against an oracle patch using SWE-RL-style diff-similarity reward.