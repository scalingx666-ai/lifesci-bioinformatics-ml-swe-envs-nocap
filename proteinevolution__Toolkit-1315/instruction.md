# Issue

**Title:** Update fs2-core, fs2-io to 3.2.0

## Description

Updates
* [co.fs2:fs2-core](https://github.com/typelevel/fs2)
* [co.fs2:fs2-io](https://github.com/typelevel/fs2)

 from 3.1.6 to 3.2.0.
[GitHub Release Notes](https://github.com/typelevel/fs2/releases/tag/v3.2.0) - [Changelog](https://github.com/typelevel/fs2/blob/master/CHANGELOG.md) - [Version Diff](https://github.com/typelevel/fs2/compare/v3.1.6...v3.2.0)

I'll automatically update this PR to resolve conflicts as long as you don't change it yourself.

If you'd like to skip this version, you can just close this PR. If you have any feedback, just mention me in the comments below.

Configure Scala Steward for your repository with a [`.scala-steward.conf`](https://github.com/scala-steward-org/scala-steward/blob/72b8131bdc169b138599359d7cef7823742891db/docs/repo-specific-configuration.md) file.

Have a fantastic day writing Scala!

<details>
<summary>Files still referring to the old version number</summary>

The following files still refer to the old version number (3.1.6).
You might want to review and update them manually.
```
frontend/yarn.lock
```
</details>
<details>
<summary>Ignore future updates</summary>

Add this to your `.scala-steward.conf` file to ignore future updates of this dependency:
```
updates.ignore = [ { groupId = "co.fs2" } ]
```
</details>

labels: library-update, semver-minor, old-version-remains

## Task

Modify the repository so that the issue described above is resolved. The repository is checked out at base commit `9e55d22d9645`. Edit files in place; the verifier captures your changes via `git diff` and scores them against an oracle patch using SWE-RL-style diff-similarity reward.