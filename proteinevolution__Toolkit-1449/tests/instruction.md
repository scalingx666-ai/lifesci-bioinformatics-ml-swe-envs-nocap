# Issue

**Title:** Update shapeless to 2.3.10

## Description

Updates [com.chuusai:shapeless](https://github.com/milessabin/shapeless) from 2.3.9 to 2.3.10.
[GitHub Release Notes](https://github.com/milessabin/shapeless/releases/tag/v2.3.10) - [Version Diff](https://github.com/milessabin/shapeless/compare/v2.3.9...v2.3.10)

I'll automatically update this PR to resolve conflicts as long as you don't change it yourself.

If you'd like to skip this version, you can just close this PR. If you have any feedback, just mention me in the comments below.

Configure Scala Steward for your repository with a [`.scala-steward.conf`](https://github.com/scala-steward-org/scala-steward/blob/fa82bbed2d8866c889e05917b319dd47ae21b08f/docs/repo-specific-configuration.md) file.

Have a fantastic day writing Scala!

<details>
<summary>Adjust future updates</summary>

Add this to your `.scala-steward.conf` file to ignore future updates of this dependency:
```
updates.ignore = [ { groupId = "com.chuusai", artifactId = "shapeless" } ]
```
Or, add this to slow down future updates of this dependency:
```
dependencyOverrides = [{
  pullRequests = { frequency = "@monthly" },
  dependency = { groupId = "com.chuusai", artifactId = "shapeless" }
}]
```
</details>

labels: library-update, early-semver-patch, semver-spec-patch, commit-count:1

## Task

Modify the repository so that the issue described above is resolved. The repository is checked out at base commit `fdc2baa58274`. Edit files in place; the verifier captures your changes via `git diff` and scores them against an oracle patch using SWE-RL-style diff-similarity reward.