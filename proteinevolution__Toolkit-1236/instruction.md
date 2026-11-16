# Issue

**Title:** Update scala-library to 2.13.6

## Description

Updates [org.scala-lang:scala-library](https://github.com/scala/scala.git) from 2.13.5 to 2.13.6.

I'll automatically update this PR to resolve conflicts as long as you don't change it yourself.

If you'd like to skip this version, you can just close this PR. If you have any feedback, just mention me in the comments below.

Configure Scala Steward for your repository with a [`.scala-steward.conf`](https://github.com/scala-steward-org/scala-steward/blob/9b1175210c902dbb63ea03d1a2136868ffb54f16/docs/repo-specific-configuration.md) file.

Have a fantastic day writing Scala!

<details>
<summary>Ignore future updates</summary>

Add this to your `.scala-steward.conf` file to ignore future updates of this dependency:
```
updates.ignore = [ { groupId = "org.scala-lang", artifactId = "scala-library" } ]
```
</details>

labels: library-update, semver-patch

## Task

Modify the repository so that the issue described above is resolved. The repository is checked out at base commit `e124380bb6a1`. Edit files in place; the verifier captures your changes via `git diff` and scores them against an oracle patch using SWE-RL-style diff-similarity reward.