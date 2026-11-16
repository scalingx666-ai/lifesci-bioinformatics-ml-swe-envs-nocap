# Issue

**Title:** Update akka-actor, akka-actor-typed, ... to 2.6.15

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

 from 2.6.14 to 2.6.15.
[GitHub Release Notes](https://github.com/akka/akka/releases/tag/v2.6.15) - [Version Diff](https://github.com/akka/akka/compare/v2.6.14...v2.6.15)

I'll automatically update this PR to resolve conflicts as long as you don't change it yourself.

If you'd like to skip this version, you can just close this PR. If you have any feedback, just mention me in the comments below.

Configure Scala Steward for your repository with a [`.scala-steward.conf`](https://github.com/scala-steward-org/scala-steward/blob/a22e8f9791b2efe63e0f6c3398044342e45b88eb/docs/repo-specific-configuration.md) file.

Have a fantastic day writing Scala!

<details>
<summary>Ignore future updates</summary>

Add this to your `.scala-steward.conf` file to ignore future updates of this dependency:
```
updates.ignore = [ { groupId = "com.typesafe.akka" } ]
```
</details>

labels: library-update, semver-patch

## Task

Modify the repository so that the issue described above is resolved. The repository is checked out at base commit `999b8e3a5f72`. Edit files in place; the verifier captures your changes via `git diff` and scores them against an oracle patch using SWE-RL-style diff-similarity reward.