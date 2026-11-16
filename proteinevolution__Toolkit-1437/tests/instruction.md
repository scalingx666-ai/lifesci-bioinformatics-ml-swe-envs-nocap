# Issue

**Title:** Update fs2-core, fs2-io to 3.2.12

## Description

Updates
* [co.fs2:fs2-core](https://github.com/typelevel/fs2)
* [co.fs2:fs2-io](https://github.com/typelevel/fs2)

 from 3.2.11 to 3.2.12.
[GitHub Release Notes](https://github.com/typelevel/fs2/releases/tag/v3.2.12) - [Version Diff](https://github.com/typelevel/fs2/compare/v3.2.11...v3.2.12)

I'll automatically update this PR to resolve conflicts as long as you don't change it yourself.

If you'd like to skip this version, you can just close this PR. If you have any feedback, just mention me in the comments below.

Configure Scala Steward for your repository with a [`.scala-steward.conf`](https://github.com/scala-steward-org/scala-steward/blob/fcd5ea3d1cd0e6506b69b5b90e21e4384162f040/docs/repo-specific-configuration.md) file.

Have a fantastic day writing Scala!

<details>
<summary>Files still referring to the old version number</summary>

The following files still refer to the old version number (3.2.11).
You might want to review and update them manually.
```
frontend/package.json
frontend/yarn.lock
```
</details>
<details>
<summary>Adjust future updates</summary>

Add this to your `.scala-steward.conf` file to ignore future updates of this dependency:
```
updates.ignore = [ { groupId = "co.fs2" } ]
```
Or, add this to slow down future updates of this dependency:
```
dependencyOverrides = [{
  pullRequests = { frequency = "@monthly" },
  dependency = { groupId = "co.fs2" }
}]
```
</details>

labels: library-update, early-semver-patch, semver-spec-patch, old-version-remains, commit-count:1

## Task

Modify the repository so that the issue described above is resolved. The repository is checked out at base commit `313791d3f31b`. Edit files in place; the verifier captures your changes via `git diff` and scores them against an oracle patch using SWE-RL-style diff-similarity reward.