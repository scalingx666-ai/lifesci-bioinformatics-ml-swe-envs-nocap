# Issue

**Title:** Update akka-actor, akka-actor-typed, ... to 2.6.18

## Description

Updates
* [com.typesafe.akka:akka-actor](https://github.com/akka/akka)
* [com.typesafe.akka:akka-actor-typed](https://github.com/akka/akka)
* [com.typesafe.akka:akka-cluster](https://github.com/akka/akka)
* [com.typesafe.akka:akka-cluster-metrics](https://github.com/akka/akka)
* [com.typesafe.akka:akka-cluster-tools](https://github.com/akka/akka)
* [com.typesafe.akka:akka-serialization-jackson](https://github.com/akka/akka)
* [com.typesafe.akka:akka-slf4j](https://github.com/akka/akka)
* [com.typesafe.akka:akka-stream](https://github.com/akka/akka)
* [com.typesafe.akka:akka-stream-testkit](https://github.com/akka/akka)
* [com.typesafe.akka:akka-testkit](https://github.com/akka/akka)

 from 2.6.15 to 2.6.18.
[GitHub Release Notes](https://github.com/akka/akka/releases/tag/v2.6.18) - [Version Diff](https://github.com/akka/akka/compare/v2.6.15...v2.6.18)

I'll automatically update this PR to resolve conflicts as long as you don't change it yourself.

If you'd like to skip this version, you can just close this PR. If you have any feedback, just mention me in the comments below.

Configure Scala Steward for your repository with a [`.scala-steward.conf`](https://github.com/scala-steward-org/scala-steward/blob/a098e2cf2f95d8c865ec1c1d8ae1685c6f5e32e1/docs/repo-specific-configuration.md) file.

Have a fantastic day writing Scala!

<details>
<summary>Ignore future updates</summary>

Add this to your `.scala-steward.conf` file to ignore future updates of this dependency:
```
updates.ignore = [ { groupId = "com.typesafe.akka" } ]
```
</details>

labels: library-update, early-semver-patch, semver-spec-patch, commit-count:1

## Task

Modify the repository so that the issue described above is resolved. The repository is checked out at base commit `36453e9973e3`. Edit files in place; the verifier captures your changes via `git diff` and scores them against an oracle patch using SWE-RL-style diff-similarity reward.