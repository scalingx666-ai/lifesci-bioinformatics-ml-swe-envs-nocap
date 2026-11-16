# Issue

**Title:** Update mockito-core to 4.5.0

## Description

Updates org.mockito:mockito-core from 4.4.0 to 4.5.0.

I'll automatically update this PR to resolve conflicts as long as you don't change it yourself.

If you'd like to skip this version, you can just close this PR. If you have any feedback, just mention me in the comments below.

Configure Scala Steward for your repository with a [`.scala-steward.conf`](https://github.com/scala-steward-org/scala-steward/blob/5ba079e5e6b075ded705306e58f3111e16796466/docs/repo-specific-configuration.md) file.

Have a fantastic day writing Scala!

<details>
<summary>Files still referring to the old version number</summary>

The following files still refer to the old version number (4.4.0).
You might want to review and update them manually.
```
frontend/yarn.lock
```
</details>
<details>
<summary>Adjust future updates</summary>

Add this to your `.scala-steward.conf` file to ignore future updates of this dependency:
```
updates.ignore = [ { groupId = "org.mockito", artifactId = "mockito-core" } ]
```
Or, add this to slow down future updates of this dependency:
```
dependencyOverrides = [{
  pullRequest = { frequency = "@monthly" },
  dependency = { groupId = "org.mockito", artifactId = "mockito-core" }
}]
```
</details>

labels: test-library-update, early-semver-minor, semver-spec-minor, old-version-remains, commit-count:1

## Task

Modify the repository so that the issue described above is resolved. The repository is checked out at base commit `6800e11f5eaf`. Edit files in place; the verifier captures your changes via `git diff` and scores them against an oracle patch using SWE-RL-style diff-similarity reward.