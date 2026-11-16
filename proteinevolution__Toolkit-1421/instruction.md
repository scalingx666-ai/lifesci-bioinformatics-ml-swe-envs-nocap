# Issue

**Title:** Update circe-generic-extras to 0.14.2

## Description

Updates [io.circe:circe-generic-extras](https://github.com/circe/circe-generic-extras) from 0.14.1 to 0.14.2.
[GitHub Release Notes](https://github.com/circe/circe-generic-extras/releases/tag/v0.14.2) - [Version Diff](https://github.com/circe/circe-generic-extras/compare/v0.14.1...v0.14.2)

I'll automatically update this PR to resolve conflicts as long as you don't change it yourself.

If you'd like to skip this version, you can just close this PR. If you have any feedback, just mention me in the comments below.

Configure Scala Steward for your repository with a [`.scala-steward.conf`](https://github.com/scala-steward-org/scala-steward/blob/fcb8d5cef00714ea0ef4f9dd18e70bce14f55e42/docs/repo-specific-configuration.md) file.

Have a fantastic day writing Scala!

<details>
<summary>Adjust future updates</summary>

Add this to your `.scala-steward.conf` file to ignore future updates of this dependency:
```
updates.ignore = [ { groupId = "io.circe", artifactId = "circe-generic-extras" } ]
```
Or, add this to slow down future updates of this dependency:
```
dependencyOverrides = [{
  pullRequests = { frequency = "@monthly" },
  dependency = { groupId = "io.circe", artifactId = "circe-generic-extras" }
}]
```
</details>

labels: library-update, early-semver-minor, semver-spec-patch, commit-count:1

## Task

Modify the repository so that the issue described above is resolved. The repository is checked out at base commit `defabc06a9c4`. Edit files in place; the verifier captures your changes via `git diff` and scores them against an oracle patch using SWE-RL-style diff-similarity reward.