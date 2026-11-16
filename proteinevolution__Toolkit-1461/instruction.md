# Issue

**Title:** Update sbt to 1.7.2

## Description

Updates [org.scala-sbt:sbt](https://github.com/sbt/sbt) from 1.7.1 to 1.7.2.
[GitHub Release Notes](https://github.com/sbt/sbt/releases/tag/v1.7.2) - [Version Diff](https://github.com/sbt/sbt/compare/v1.7.1...v1.7.2)

I'll automatically update this PR to resolve conflicts as long as you don't change it yourself.

If you'd like to skip this version, you can just close this PR. If you have any feedback, just mention me in the comments below.

Configure Scala Steward for your repository with a [`.scala-steward.conf`](https://github.com/scala-steward-org/scala-steward/blob/f90f842deb5579a7a9793371fef17ba7c79c8e5f/docs/repo-specific-configuration.md) file.

Have a fantastic day writing Scala!

<details>
<summary>Adjust future updates</summary>

Add this to your `.scala-steward.conf` file to ignore future updates of this dependency:
```
updates.ignore = [ { groupId = "org.scala-sbt", artifactId = "sbt" } ]
```
Or, add this to slow down future updates of this dependency:
```
dependencyOverrides = [{
  pullRequests = { frequency = "@monthly" },
  dependency = { groupId = "org.scala-sbt", artifactId = "sbt" }
}]
```
</details>

labels: library-update, early-semver-patch, semver-spec-patch, commit-count:1

## Task

Modify the repository so that the issue described above is resolved. The repository is checked out at base commit `6fe04cba68e3`. Edit files in place; the verifier captures your changes via `git diff` and scores them against an oracle patch using SWE-RL-style diff-similarity reward.