# Issue

**Title:** Update sbt to 1.5.6

## Description

Updates [org.scala-sbt:sbt](https://github.com/sbt/sbt) from 1.5.5 to 1.5.6.
[GitHub Release Notes](https://github.com/sbt/sbt/releases/tag/v1.5.6) - [Version Diff](https://github.com/sbt/sbt/compare/v1.5.5...v1.5.6)

I'll automatically update this PR to resolve conflicts as long as you don't change it yourself.

If you'd like to skip this version, you can just close this PR. If you have any feedback, just mention me in the comments below.

Configure Scala Steward for your repository with a [`.scala-steward.conf`](https://github.com/scala-steward-org/scala-steward/blob/c53805c421eed74f6fe9f0227c587ff230f7803f/docs/repo-specific-configuration.md) file.

Have a fantastic day writing Scala!

<details>
<summary>Files still referring to the old version number</summary>

The following files still refer to the old version number (1.5.5).
You might want to review and update them manually.
```
frontend/yarn.lock
```
</details>
<details>
<summary>Ignore future updates</summary>

Add this to your `.scala-steward.conf` file to ignore future updates of this dependency:
```
updates.ignore = [ { groupId = "org.scala-sbt", artifactId = "sbt" } ]
```
</details>

labels: library-update, early-semver-patch, semver-spec-patch, old-version-remains, commit-count:1

## Task

Modify the repository so that the issue described above is resolved. The repository is checked out at base commit `9fe22ca553e4`. Edit files in place; the verifier captures your changes via `git diff` and scores them against an oracle patch using SWE-RL-style diff-similarity reward.