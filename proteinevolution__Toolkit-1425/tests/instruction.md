# Issue

**Title:** Update cats-core to 2.8.0

## Description

Updates [org.typelevel:cats-core](https://github.com/typelevel/cats) from 2.7.0 to 2.8.0.
[GitHub Release Notes](https://github.com/typelevel/cats/releases/tag/v2.8.0) - [Version Diff](https://github.com/typelevel/cats/compare/v2.7.0...v2.8.0)

I'll automatically update this PR to resolve conflicts as long as you don't change it yourself.

If you'd like to skip this version, you can just close this PR. If you have any feedback, just mention me in the comments below.

Configure Scala Steward for your repository with a [`.scala-steward.conf`](https://github.com/scala-steward-org/scala-steward/blob/fcb8d5cef00714ea0ef4f9dd18e70bce14f55e42/docs/repo-specific-configuration.md) file.

Have a fantastic day writing Scala!

<details>
<summary>Files still referring to the old version number</summary>

The following files still refer to the old version number (2.7.0).
You might want to review and update them manually.
```
frontend/yarn.lock
```
</details>
<details>
<summary>Adjust future updates</summary>

Add this to your `.scala-steward.conf` file to ignore future updates of this dependency:
```
updates.ignore = [ { groupId = "org.typelevel", artifactId = "cats-core" } ]
```
Or, add this to slow down future updates of this dependency:
```
dependencyOverrides = [{
  pullRequests = { frequency = "@monthly" },
  dependency = { groupId = "org.typelevel", artifactId = "cats-core" }
}]
```
</details>

labels: library-update, early-semver-minor, semver-spec-minor, old-version-remains, commit-count:1

## Task

Modify the repository so that the issue described above is resolved. The repository is checked out at base commit `defabc06a9c4`. Edit files in place; the verifier captures your changes via `git diff` and scores them against an oracle patch using SWE-RL-style diff-similarity reward.