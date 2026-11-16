# Issue

**Title:** Update reactivemongo-akkastream to 1.0.4

## Description

Updates [org.reactivemongo:reactivemongo-akkastream](http://reactivemongo.org) from 1.0.3 to 1.0.4.

I'll automatically update this PR to resolve conflicts as long as you don't change it yourself.

If you'd like to skip this version, you can just close this PR. If you have any feedback, just mention me in the comments below.

Configure Scala Steward for your repository with a [`.scala-steward.conf`](https://github.com/scala-steward-org/scala-steward/blob/9b1175210c902dbb63ea03d1a2136868ffb54f16/docs/repo-specific-configuration.md) file.

Have a fantastic day writing Scala!

<details>
<summary>Files still referring to the old version number</summary>

The following files still refer to the old version number (1.0.3).
You might want to review and update them manually.
```
frontend/package.json
frontend/yarn.lock
project/Dependencies.scala
```
</details>
<details>
<summary>Ignore future updates</summary>

Add this to your `.scala-steward.conf` file to ignore future updates of this dependency:
```
updates.ignore = [ { groupId = "org.reactivemongo", artifactId = "reactivemongo-akkastream" } ]
```
</details>

labels: library-update, semver-patch, old-version-remains

## Task

Modify the repository so that the issue described above is resolved. The repository is checked out at base commit `201e1f541dea`. Edit files in place; the verifier captures your changes via `git diff` and scores them against an oracle patch using SWE-RL-style diff-similarity reward.