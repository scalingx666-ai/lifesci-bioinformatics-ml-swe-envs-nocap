# Issue

**Title:** Update fs2-core, fs2-io to 3.2.2

## Description

Updates
* [co.fs2:fs2-core](https://github.com/typelevel/fs2)
* [co.fs2:fs2-io](https://github.com/typelevel/fs2)

 from 3.2.1 to 3.2.2.
[GitHub Release Notes](https://github.com/typelevel/fs2/releases/tag/v3.2.2) - [Changelog](https://github.com/typelevel/fs2/blob/master/CHANGELOG.md) - [Version Diff](https://github.com/typelevel/fs2/compare/v3.2.1...v3.2.2)

I'll automatically update this PR to resolve conflicts as long as you don't change it yourself.

If you'd like to skip this version, you can just close this PR. If you have any feedback, just mention me in the comments below.

Configure Scala Steward for your repository with a [`.scala-steward.conf`](https://github.com/scala-steward-org/scala-steward/blob/3dbb798609a684b5279e72500d71e915c2423962/docs/repo-specific-configuration.md) file.

Have a fantastic day writing Scala!

<details>
<summary>Files still referring to the old version number</summary>

The following files still refer to the old version number (3.2.1).
You might want to review and update them manually.
```
frontend/package.json
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

labels: library-update, early-semver-patch, semver-spec-patch, old-version-remains

## Task

Modify the repository so that the issue described above is resolved. The repository is checked out at base commit `a86f339f8401`. Edit files in place; the verifier captures your changes via `git diff` and scores them against an oracle patch using SWE-RL-style diff-similarity reward.