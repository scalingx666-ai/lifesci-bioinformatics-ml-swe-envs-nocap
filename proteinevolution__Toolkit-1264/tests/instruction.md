# Issue

**Title:** Update play2-reactivemongo to 1.0.5-play28

## Description

Updates [org.reactivemongo:play2-reactivemongo](https://github.com/cchantep/Play-ReactiveMongo.git) from 1.0.4-play28 to 1.0.5-play28.

I'll automatically update this PR to resolve conflicts as long as you don't change it yourself.

If you'd like to skip this version, you can just close this PR. If you have any feedback, just mention me in the comments below.

Configure Scala Steward for your repository with a [`.scala-steward.conf`](https://github.com/scala-steward-org/scala-steward/blob/e9b7ea8e42cbd4d14a7b8a7af78f40f8008efdc0/docs/repo-specific-configuration.md) file.

Have a fantastic day writing Scala!

<details>
<summary>Ignore future updates</summary>

Add this to your `.scala-steward.conf` file to ignore future updates of this dependency:
```
updates.ignore = [ { groupId = "org.reactivemongo", artifactId = "play2-reactivemongo" } ]
```
</details>

labels: library-update, semver-patch

## Task

Modify the repository so that the issue described above is resolved. The repository is checked out at base commit `82b5778c00f5`. Edit files in place; the verifier captures your changes via `git diff` and scores them against an oracle patch using SWE-RL-style diff-similarity reward.