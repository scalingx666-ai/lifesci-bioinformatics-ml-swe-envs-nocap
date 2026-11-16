# Issue

**Title:** Update scalafmt-core to 3.6.0

## Description

Updates [org.scalameta:scalafmt-core](https://github.com/scalameta/scalafmt) from 3.5.9 to 3.6.0.
[GitHub Release Notes](https://github.com/scalameta/scalafmt/releases/tag/v3.6.0) - [Version Diff](https://github.com/scalameta/scalafmt/compare/v3.5.9...v3.6.0)

I'll automatically update this PR to resolve conflicts as long as you don't change it yourself.

If you'd like to skip this version, you can just close this PR. If you have any feedback, just mention me in the comments below.

Configure Scala Steward for your repository with a [`.scala-steward.conf`](https://github.com/scala-steward-org/scala-steward/blob/f90f842deb5579a7a9793371fef17ba7c79c8e5f/docs/repo-specific-configuration.md) file.

Have a fantastic day writing Scala!

<details>
<summary>Adjust future updates</summary>

Add this to your `.scala-steward.conf` file to ignore future updates of this dependency:
```
updates.ignore = [ { groupId = "org.scalameta", artifactId = "scalafmt-core" } ]
```
Or, add this to slow down future updates of this dependency:
```
dependencyOverrides = [{
  pullRequests = { frequency = "@monthly" },
  dependency = { groupId = "org.scalameta", artifactId = "scalafmt-core" }
}]
```
</details>

labels: library-update, early-semver-minor, semver-spec-minor, commit-count:n:3

## Task

Modify the repository so that the issue described above is resolved. The repository is checked out at base commit `6fe04cba68e3`. Edit files in place; the verifier captures your changes via `git diff` and scores them against an oracle patch using SWE-RL-style diff-similarity reward.