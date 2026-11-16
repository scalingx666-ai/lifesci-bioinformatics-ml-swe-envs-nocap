# Issue

**Title:** Update sbt-header to 5.7.0

## Description

Updates [de.heikoseeberger:sbt-header](https://github.com/sbt/sbt-header) from 5.6.5 to 5.7.0.
[GitHub Release Notes](https://github.com/sbt/sbt-header/releases/tag/v5.7.0) - [Version Diff](https://github.com/sbt/sbt-header/compare/v5.6.5...v5.7.0)

I'll automatically update this PR to resolve conflicts as long as you don't change it yourself.

If you'd like to skip this version, you can just close this PR. If you have any feedback, just mention me in the comments below.

Configure Scala Steward for your repository with a [`.scala-steward.conf`](https://github.com/scala-steward-org/scala-steward/blob/5ba079e5e6b075ded705306e58f3111e16796466/docs/repo-specific-configuration.md) file.

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
  pullRequest = { frequency = "@monthly" },
  dependency = { groupId = "de.heikoseeberger", artifactId = "sbt-header" }
}]
```
</details>

labels: sbt-plugin-update, early-semver-minor, semver-spec-minor, commit-count:1

## Task

Modify the repository so that the issue described above is resolved. The repository is checked out at base commit `a6f0c5385193`. Edit files in place; the verifier captures your changes via `git diff` and scores them against an oracle patch using SWE-RL-style diff-similarity reward.