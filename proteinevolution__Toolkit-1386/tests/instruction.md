# Issue

**Title:** Update sbt-buildinfo to 0.11.0

## Description

Updates [com.eed3si9n:sbt-buildinfo](https://github.com/sbt/sbt-buildinfo) from 0.10.0 to 0.11.0.
[GitHub Release Notes](https://github.com/sbt/sbt-buildinfo/releases/tag/v0.11.0) - [Version Diff](https://github.com/sbt/sbt-buildinfo/compare/v0.10.0...v0.11.0)

I'll automatically update this PR to resolve conflicts as long as you don't change it yourself.

If you'd like to skip this version, you can just close this PR. If you have any feedback, just mention me in the comments below.

Configure Scala Steward for your repository with a [`.scala-steward.conf`](https://github.com/scala-steward-org/scala-steward/blob/97ef5956853b9dd4bc8469e71d9c6e077ad04f0a/docs/repo-specific-configuration.md) file.

Have a fantastic day writing Scala!

<details>
<summary>Files still referring to the old version number</summary>

The following files still refer to the old version number (0.10.0).
You might want to review and update them manually.
```
frontend/yarn.lock
```
</details>
<details>
<summary>Ignore future updates</summary>

Add this to your `.scala-steward.conf` file to ignore future updates of this dependency:
```
updates.ignore = [ { groupId = "com.eed3si9n", artifactId = "sbt-buildinfo" } ]
```
</details>

labels: sbt-plugin-update, early-semver-major, semver-spec-minor, old-version-remains, commit-count:1

## Task

Modify the repository so that the issue described above is resolved. The repository is checked out at base commit `12e4570f33b0`. Edit files in place; the verifier captures your changes via `git diff` and scores them against an oracle patch using SWE-RL-style diff-similarity reward.