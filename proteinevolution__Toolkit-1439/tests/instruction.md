# Issue

**Title:** Update scalafmt-core to 3.5.9

## Description

Updates [org.scalameta:scalafmt-core](https://github.com/scalameta/scalafmt) from 3.5.8 to 3.5.9.
[GitHub Release Notes](https://github.com/scalameta/scalafmt/releases/tag/v3.5.9) - [Version Diff](https://github.com/scalameta/scalafmt/compare/v3.5.8...v3.5.9)

I'll automatically update this PR to resolve conflicts as long as you don't change it yourself.

If you'd like to skip this version, you can just close this PR. If you have any feedback, just mention me in the comments below.

Configure Scala Steward for your repository with a [`.scala-steward.conf`](https://github.com/scala-steward-org/scala-steward/blob/a2954c3d09f9ed01aaed377a0674aba5a60f90e5/docs/repo-specific-configuration.md) file.

Have a fantastic day writing Scala!

<details>
<summary>Files still referring to the old version number</summary>

The following files still refer to the old version number (3.5.8).
You might want to review and update them manually.
```
.git-blame-ignore-revs
```
</details>
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

labels: library-update, early-semver-patch, semver-spec-patch, old-version-remains, commit-count:1

## Task

Modify the repository so that the issue described above is resolved. The repository is checked out at base commit `313791d3f31b`. Edit files in place; the verifier captures your changes via `git diff` and scores them against an oracle patch using SWE-RL-style diff-similarity reward.