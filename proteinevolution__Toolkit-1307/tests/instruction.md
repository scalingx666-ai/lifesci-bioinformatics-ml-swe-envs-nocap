# Issue

**Title:** Update mockito-core to 4.0.0

## Description

Updates [org.mockito:mockito-core](https://github.com/mockito/mockito.git) from 3.12.4 to 4.0.0.

I'll automatically update this PR to resolve conflicts as long as you don't change it yourself.

If you'd like to skip this version, you can just close this PR. If you have any feedback, just mention me in the comments below.

Configure Scala Steward for your repository with a [`.scala-steward.conf`](https://github.com/scala-steward-org/scala-steward/blob/5a8bcab5f49db803d24f965706806e9d59d59e11/docs/repo-specific-configuration.md) file.

Have a fantastic day writing Scala!

<details>
<summary>Ignore future updates</summary>

Add this to your `.scala-steward.conf` file to ignore future updates of this dependency:
```
updates.ignore = [ { groupId = "org.mockito", artifactId = "mockito-core" } ]
```
</details>

labels: test-library-update, semver-major

## Task

Modify the repository so that the issue described above is resolved. The repository is checked out at base commit `f0c71743e52f`. Edit files in place; the verifier captures your changes via `git diff` and scores them against an oracle patch using SWE-RL-style diff-similarity reward.