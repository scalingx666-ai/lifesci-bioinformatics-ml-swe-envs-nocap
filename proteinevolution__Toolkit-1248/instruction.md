# Issue

**Title:** Update mockito-core to 3.11.0

## Description

Updates [org.mockito:mockito-core](https://github.com/mockito/mockito.git) from 3.10.0 to 3.11.0.

I'll automatically update this PR to resolve conflicts as long as you don't change it yourself.

If you'd like to skip this version, you can just close this PR. If you have any feedback, just mention me in the comments below.

Configure Scala Steward for your repository with a [`.scala-steward.conf`](https://github.com/scala-steward-org/scala-steward/blob/4ec2dc0d3b3b79c1a0b8f88f274fd72451dc5fe6/docs/repo-specific-configuration.md) file.

Have a fantastic day writing Scala!

<details>
<summary>Ignore future updates</summary>

Add this to your `.scala-steward.conf` file to ignore future updates of this dependency:
```
updates.ignore = [ { groupId = "org.mockito", artifactId = "mockito-core" } ]
```
</details>

labels: test-library-update, semver-minor

## Task

Modify the repository so that the issue described above is resolved. The repository is checked out at base commit `1d8444eabffd`. Edit files in place; the verifier captures your changes via `git diff` and scores them against an oracle patch using SWE-RL-style diff-similarity reward.