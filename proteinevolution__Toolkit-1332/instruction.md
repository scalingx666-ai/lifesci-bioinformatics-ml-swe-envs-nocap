# Issue

**Title:** Update filters-helpers, play-ahc-ws, ... to 2.8.10

## Description

Updates
* [com.typesafe.play:filters-helpers](https://github.com/playframework/playframework)
* [com.typesafe.play:play-ahc-ws](https://github.com/playframework/playframework)
* [com.typesafe.play:play-akka-http-server](https://github.com/playframework/playframework)
* [com.typesafe.play:play-akka-http2-support](https://github.com/playframework/playframework)
* [com.typesafe.play:play-docs](https://github.com/playframework/playframework)
* [com.typesafe.play:play-ehcache](https://github.com/playframework/playframework)
* [com.typesafe.play:play-guice](https://github.com/playframework/playframework)
* [com.typesafe.play:play-logback](https://github.com/playframework/playframework)
* [com.typesafe.play:play-server](https://github.com/playframework/playframework)
* [com.typesafe.play:play-test](https://github.com/playframework/playframework)
* [com.typesafe.play:sbt-plugin](https://github.com/playframework/playframework)

 from 2.8.8 to 2.8.10.

I'll automatically update this PR to resolve conflicts as long as you don't change it yourself.

If you'd like to skip this version, you can just close this PR. If you have any feedback, just mention me in the comments below.

Configure Scala Steward for your repository with a [`.scala-steward.conf`](https://github.com/scala-steward-org/scala-steward/blob/4f27bc444ee87b1925ccb4cf714e72eebe9763ab/docs/repo-specific-configuration.md) file.

Have a fantastic day writing Scala!

<details>
<summary>Ignore future updates</summary>

Add this to your `.scala-steward.conf` file to ignore future updates of this dependency:
```
updates.ignore = [ { groupId = "com.typesafe.play" } ]
```
</details>

labels: library-update, early-semver-patch, semver-spec-patch

## Task

Modify the repository so that the issue described above is resolved. The repository is checked out at base commit `f6566fe6cdba`. Edit files in place; the verifier captures your changes via `git diff` and scores them against an oracle patch using SWE-RL-style diff-similarity reward.