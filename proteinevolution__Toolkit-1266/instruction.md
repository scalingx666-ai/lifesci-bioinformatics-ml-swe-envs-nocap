# Issue

**Title:** Update macros to 2.4.0

## Description

Updates [com.softwaremill.macwire:macros](https://github.com/softwaremill/macwire) from 2.3.7 to 2.4.0.
[GitHub Release Notes](https://github.com/softwaremill/macwire/releases/tag/v2.4.0)

I'll automatically update this PR to resolve conflicts as long as you don't change it yourself.

If you'd like to skip this version, you can just close this PR. If you have any feedback, just mention me in the comments below.

Configure Scala Steward for your repository with a [`.scala-steward.conf`](https://github.com/scala-steward-org/scala-steward/blob/dac0e268a872ebbc9c6763788c1ca51bf05b5d99/docs/repo-specific-configuration.md) file.

Have a fantastic day writing Scala!

<details>
<summary>Files still referring to the old version number</summary>

The following files still refer to the old version number (2.3.7).
You might want to review and update them manually.
```
frontend/yarn.lock
project/Dependencies.scala
```
</details>
<details>
<summary>Ignore future updates</summary>

Add this to your `.scala-steward.conf` file to ignore future updates of this dependency:
```
updates.ignore = [ { groupId = "com.softwaremill.macwire", artifactId = "macros" } ]
```
</details>

labels: test-library-update, semver-minor, old-version-remains

## Task

Modify the repository so that the issue described above is resolved. The repository is checked out at base commit `d8eefd526d2a`. Edit files in place; the verifier captures your changes via `git diff` and scores them against an oracle patch using SWE-RL-style diff-similarity reward.