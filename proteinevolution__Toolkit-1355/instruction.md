# Issue

**Title:** Update sbt to 1.6.1

## Description

Updates [org.scala-sbt:sbt](https://github.com/sbt/sbt) from 1.5.8 to 1.6.1.

I'll automatically update this PR to resolve conflicts as long as you don't change it yourself.

If you'd like to skip this version, you can just close this PR. If you have any feedback, just mention me in the comments below.

Configure Scala Steward for your repository with a [`.scala-steward.conf`](https://github.com/scala-steward-org/scala-steward/blob/9b1c09f5f987bb5fed4240c3187029c020caae24/docs/repo-specific-configuration.md) file.

Have a fantastic day writing Scala!

<details>
<summary>Ignore future updates</summary>

Add this to your `.scala-steward.conf` file to ignore future updates of this dependency:
```
updates.ignore = [ { groupId = "org.scala-sbt", artifactId = "sbt" } ]
```
</details>

labels: library-update, early-semver-minor, semver-spec-minor, commit-count:1

## Task

Modify the repository so that the issue described above is resolved. The repository is checked out at base commit `b921cfbd79cf`. Edit files in place; the verifier captures your changes via `git diff` and scores them against an oracle patch using SWE-RL-style diff-similarity reward.