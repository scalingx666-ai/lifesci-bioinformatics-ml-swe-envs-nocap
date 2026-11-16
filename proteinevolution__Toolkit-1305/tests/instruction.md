# Issue

**Title:** Update fs2-core, fs2-io to 3.1.4

## Description

Updates
* [co.fs2:fs2-core](https://github.com/typelevel/fs2)
* [co.fs2:fs2-io](https://github.com/typelevel/fs2)

 from 3.1.3 to 3.1.4.
[GitHub Release Notes](https://github.com/typelevel/fs2/releases/tag/v3.1.4) - [Changelog](https://github.com/typelevel/fs2/blob/master/CHANGELOG.md) - [Version Diff](https://github.com/typelevel/fs2/compare/v3.1.3...v3.1.4)

I'll automatically update this PR to resolve conflicts as long as you don't change it yourself.

If you'd like to skip this version, you can just close this PR. If you have any feedback, just mention me in the comments below.

Configure Scala Steward for your repository with a [`.scala-steward.conf`](https://github.com/scala-steward-org/scala-steward/blob/b4bdb685a36b5efc465aff80136f8800adf28834/docs/repo-specific-configuration.md) file.

Have a fantastic day writing Scala!

<details>
<summary>Files still referring to the old version number</summary>

The following files still refer to the old version number (3.1.3).
You might want to review and update them manually.
```
conf/blacklist.conf
frontend/src/i18n/lang/extras/modals/toolHelp/backtrans.ts
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

labels: library-update, semver-patch, old-version-remains

## Task

Modify the repository so that the issue described above is resolved. The repository is checked out at base commit `42f4f25aad3a`. Edit files in place; the verifier captures your changes via `git diff` and scores them against an oracle patch using SWE-RL-style diff-similarity reward.