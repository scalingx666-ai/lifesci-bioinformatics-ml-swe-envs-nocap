# Issue

**Title:** Update sbt-header to 5.8.0

## Description

Updates [de.heikoseeberger:sbt-header](https://github.com/sbt/sbt-header) from 5.7.0 to 5.8.0.
[GitHub Release Notes](https://github.com/sbt/sbt-header/releases/tag/v5.8.0) - [Version Diff](https://github.com/sbt/sbt-header/compare/v5.7.0...v5.8.0)

I'll automatically update this PR to resolve conflicts as long as you don't change it yourself.

If you'd like to skip this version, you can just close this PR. If you have any feedback, just mention me in the comments below.

Configure Scala Steward for your repository with a [`.scala-steward.conf`](https://github.com/scala-steward-org/scala-steward/blob/f90f842deb5579a7a9793371fef17ba7c79c8e5f/docs/repo-specific-configuration.md) file.

Have a fantastic day writing Scala!

<details>
<summary>Adjust future updates</summary>

Add this to your `.scala-steward.conf` file to ignore future updates of this dependency:
```
updates.ignore = [ { groupId = "de.heikoseeberger", artifactId = "sbt-header" } ]
```
Or, add this to slow down future updates of this dependency:
```
dependencyOverrides = [{
  pullRequests = { frequency = "@monthly" },
  dependency = { groupId = "de.heikoseeberger", artifactId = "sbt-header" }
}]
```
</details>

labels: sbt-plugin-update, early-semver-minor, semver-spec-minor, commit-count:1

## Task

Modify the repository so that the issue described above is resolved. The repository is checked out at base commit `6fe04cba68e3`. Edit files in place; the verifier captures your changes via `git diff` and scores them against an oracle patch using SWE-RL-style diff-similarity reward.