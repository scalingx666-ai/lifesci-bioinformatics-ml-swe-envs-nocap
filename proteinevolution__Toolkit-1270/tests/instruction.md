# Issue

**Title:** Update reactivemongo-akkastream to 1.0.6

## Description

Updates [org.reactivemongo:reactivemongo-akkastream](http://reactivemongo.org) from 1.0.5 to 1.0.6.

I'll automatically update this PR to resolve conflicts as long as you don't change it yourself.

If you'd like to skip this version, you can just close this PR. If you have any feedback, just mention me in the comments below.

Configure Scala Steward for your repository with a [`.scala-steward.conf`](https://github.com/scala-steward-org/scala-steward/blob/626741b08458f6387252008f042f7700a8ce49e5/docs/repo-specific-configuration.md) file.

Have a fantastic day writing Scala!

<details>
<summary>Files still referring to the old version number</summary>

The following files still refer to the old version number (1.0.5).
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

Modify the repository so that the issue described above is resolved. The repository is checked out at base commit `0be46dd19eda`. Edit files in place; the verifier captures your changes via `git diff` and scores them against an oracle patch using SWE-RL-style diff-similarity reward.