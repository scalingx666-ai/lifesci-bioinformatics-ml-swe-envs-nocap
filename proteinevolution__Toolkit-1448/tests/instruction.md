# Issue

**Title:** Update mockito-core to 4.8.0

## Description

Updates org.mockito:mockito-core from 4.7.0 to 4.8.0.

I'll automatically update this PR to resolve conflicts as long as you don't change it yourself.

If you'd like to skip this version, you can just close this PR. If you have any feedback, just mention me in the comments below.

Configure Scala Steward for your repository with a [`.scala-steward.conf`](https://github.com/scala-steward-org/scala-steward/blob/7e312bd5eb80edddc58c6aeb5bfb589a8d1d8708/docs/repo-specific-configuration.md) file.

Have a fantastic day writing Scala!

<details>
<summary>Adjust future updates</summary>

Add this to your `.scala-steward.conf` file to ignore future updates of this dependency:
```
updates.ignore = [ { groupId = "org.mockito", artifactId = "mockito-core" } ]
```
Or, add this to slow down future updates of this dependency:
```
dependencyOverrides = [{
  pullRequests = { frequency = "@monthly" },
  dependency = { groupId = "org.mockito", artifactId = "mockito-core" }
}]
```
</details>

labels: test-library-update, early-semver-minor, semver-spec-minor, commit-count:1

## Task

Modify the repository so that the issue described above is resolved. The repository is checked out at base commit `4f1b335cffb1`. Edit files in place; the verifier captures your changes via `git diff` and scores them against an oracle patch using SWE-RL-style diff-similarity reward.