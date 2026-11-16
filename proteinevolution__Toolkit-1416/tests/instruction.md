# Issue

**Title:** Update cats-effect to 3.3.12

## Description

Updates [org.typelevel:cats-effect](https://github.com/typelevel/cats-effect) from 3.3.11 to 3.3.12.
[GitHub Release Notes](https://github.com/typelevel/cats-effect/releases/tag/v3.3.12) - [Version Diff](https://github.com/typelevel/cats-effect/compare/v3.3.11...v3.3.12)

I'll automatically update this PR to resolve conflicts as long as you don't change it yourself.

If you'd like to skip this version, you can just close this PR. If you have any feedback, just mention me in the comments below.

Configure Scala Steward for your repository with a [`.scala-steward.conf`](https://github.com/scala-steward-org/scala-steward/blob/960ae4bc18b810654be1e11f8848eb3b280cac64/docs/repo-specific-configuration.md) file.

Have a fantastic day writing Scala!

<details>
<summary>Adjust future updates</summary>

Add this to your `.scala-steward.conf` file to ignore future updates of this dependency:
```
updates.ignore = [ { groupId = "org.typelevel", artifactId = "cats-effect" } ]
```
Or, add this to slow down future updates of this dependency:
```
dependencyOverrides = [{
  pullRequests = { frequency = "@monthly" },
  dependency = { groupId = "org.typelevel", artifactId = "cats-effect" }
}]
```
</details>

labels: library-update, early-semver-patch, semver-spec-patch, commit-count:1

## Task

Modify the repository so that the issue described above is resolved. The repository is checked out at base commit `ae5c4dae3f42`. Edit files in place; the verifier captures your changes via `git diff` and scores them against an oracle patch using SWE-RL-style diff-similarity reward.