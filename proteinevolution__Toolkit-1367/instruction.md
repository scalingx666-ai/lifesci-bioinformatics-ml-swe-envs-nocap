# Issue

**Title:** Update macros to 2.5.4

## Description

Updates [com.softwaremill.macwire:macros](https://github.com/softwaremill/macwire) from 2.5.3 to 2.5.4.
[GitHub Release Notes](https://github.com/softwaremill/macwire/releases/tag/v2.5.4) - [Version Diff](https://github.com/softwaremill/macwire/compare/v2.5.3...v2.5.4)

I'll automatically update this PR to resolve conflicts as long as you don't change it yourself.

If you'd like to skip this version, you can just close this PR. If you have any feedback, just mention me in the comments below.

Configure Scala Steward for your repository with a [`.scala-steward.conf`](https://github.com/scala-steward-org/scala-steward/blob/dbf751df5095f57e6a58e06e9022496593536ce0/docs/repo-specific-configuration.md) file.

Have a fantastic day writing Scala!

<details>
<summary>Ignore future updates</summary>

Add this to your `.scala-steward.conf` file to ignore future updates of this dependency:
```
updates.ignore = [ { groupId = "com.softwaremill.macwire", artifactId = "macros" } ]
```
</details>

labels: test-library-update, early-semver-patch, semver-spec-patch, commit-count:1

## Task

Modify the repository so that the issue described above is resolved. The repository is checked out at base commit `5bc552b5a5f5`. Edit files in place; the verifier captures your changes via `git diff` and scores them against an oracle patch using SWE-RL-style diff-similarity reward.