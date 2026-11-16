# Issue

**Title:** Update filters-helpers, play-ahc-ws, ... to 2.8.18

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

 from 2.8.17 to 2.8.18.
[GitHub Release Notes](https://github.com/playframework/playframework/releases/tag/2.8.18) - [Version Diff](https://github.com/playframework/playframework/compare/2.8.17...2.8.18)

I'll automatically update this PR to resolve conflicts as long as you don't change it yourself.

If you'd like to skip this version, you can just close this PR. If you have any feedback, just mention me in the comments below.

Configure Scala Steward for your repository with a [`.scala-steward.conf`](https://github.com/scala-steward-org/scala-steward/blob/f90f842deb5579a7a9793371fef17ba7c79c8e5f/docs/repo-specific-configuration.md) file.

Have a fantastic day writing Scala!

<details>
<summary>Adjust future updates</summary>

Add this to your `.scala-steward.conf` file to ignore future updates of this dependency:
```
updates.ignore = [ { groupId = "com.typesafe.play" } ]
```
Or, add this to slow down future updates of this dependency:
```
dependencyOverrides = [{
  pullRequests = { frequency = "@monthly" },
  dependency = { groupId = "com.typesafe.play" }
}]
```
</details>

labels: library-update, early-semver-patch, semver-spec-patch, commit-count:1

## Task

Modify the repository so that the issue described above is resolved. The repository is checked out at base commit `6fe04cba68e3`. Edit files in place; the verifier captures your changes via `git diff` and scores them against an oracle patch using SWE-RL-style diff-similarity reward.