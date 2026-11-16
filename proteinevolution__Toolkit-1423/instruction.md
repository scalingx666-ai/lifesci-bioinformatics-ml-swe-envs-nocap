# Issue

**Title:** Update scalafmt-core to 3.5.8

## Description

Updates [org.scalameta:scalafmt-core](https://github.com/scalameta/scalafmt) from 3.5.2 to 3.5.8.
[GitHub Release Notes](https://github.com/scalameta/scalafmt/releases/tag/v3.5.8) - [Version Diff](https://github.com/scalameta/scalafmt/compare/v3.5.2...v3.5.8)

I'll automatically update this PR to resolve conflicts as long as you don't change it yourself.

If you'd like to skip this version, you can just close this PR. If you have any feedback, just mention me in the comments below.

Configure Scala Steward for your repository with a [`.scala-steward.conf`](https://github.com/scala-steward-org/scala-steward/blob/fcb8d5cef00714ea0ef4f9dd18e70bce14f55e42/docs/repo-specific-configuration.md) file.

Have a fantastic day writing Scala!

<details>
<summary>Files still referring to the old version number</summary>

The following files still refer to the old version number (3.5.2).
You might want to review and update them manually.
```
frontend/yarn.lock
tel/env/environment.sh
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

labels: library-update, early-semver-patch, semver-spec-patch, old-version-remains, commit-count:n:3

## Task

Modify the repository so that the issue described above is resolved. The repository is checked out at base commit `defabc06a9c4`. Edit files in place; the verifier captures your changes via `git diff` and scores them against an oracle patch using SWE-RL-style diff-similarity reward.