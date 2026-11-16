# Issue

**Title:** Update fs2-core, fs2-io to 3.2.11

## Description

Updates
* [co.fs2:fs2-core](https://github.com/typelevel/fs2)
* [co.fs2:fs2-io](https://github.com/typelevel/fs2)

 from 3.2.10 to 3.2.11.
[GitHub Release Notes](https://github.com/typelevel/fs2/releases/tag/v3.2.11) - [Version Diff](https://github.com/typelevel/fs2/compare/v3.2.10...v3.2.11)

I'll automatically update this PR to resolve conflicts as long as you don't change it yourself.

If you'd like to skip this version, you can just close this PR. If you have any feedback, just mention me in the comments below.

Configure Scala Steward for your repository with a [`.scala-steward.conf`](https://github.com/scala-steward-org/scala-steward/blob/54019bdd216034813f3245f57b2d5d3a23399efb/docs/repo-specific-configuration.md) file.

Have a fantastic day writing Scala!

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

labels: library-update, early-semver-patch, semver-spec-patch, commit-count:1

## Task

Modify the repository so that the issue described above is resolved. The repository is checked out at base commit `90c1ed735e5b`. Edit files in place; the verifier captures your changes via `git diff` and scores them against an oracle patch using SWE-RL-style diff-similarity reward.