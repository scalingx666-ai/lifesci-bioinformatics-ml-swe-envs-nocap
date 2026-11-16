# Issue

**Title:** Update macros to 2.5.8

## Description

Updates [com.softwaremill.macwire:macros](https://github.com/softwaremill/macwire) from 2.5.7 to 2.5.8.
[GitHub Release Notes](https://github.com/softwaremill/macwire/releases/tag/v2.5.8) - [Version Diff](https://github.com/softwaremill/macwire/compare/v2.5.7...v2.5.8)

I'll automatically update this PR to resolve conflicts as long as you don't change it yourself.

If you'd like to skip this version, you can just close this PR. If you have any feedback, just mention me in the comments below.

Configure Scala Steward for your repository with a [`.scala-steward.conf`](https://github.com/scala-steward-org/scala-steward/blob/f35fcd6c4246f706e22e281271be6815cdcc60ca/docs/repo-specific-configuration.md) file.

Have a fantastic day writing Scala!

<details>
<summary>Adjust future updates</summary>

Add this to your `.scala-steward.conf` file to ignore future updates of this dependency:
```
updates.ignore = [ { groupId = "com.softwaremill.macwire", artifactId = "macros" } ]
```
Or, add this to slow down future updates of this dependency:
```
dependencyOverrides = [{
  pullRequests = { frequency = "@monthly" },
  dependency = { groupId = "com.softwaremill.macwire", artifactId = "macros" }
}]
```
</details>

labels: test-library-update, early-semver-patch, semver-spec-patch, commit-count:1

## Task

Modify the repository so that the issue described above is resolved. The repository is checked out at base commit `2d057b9affc4`. Edit files in place; the verifier captures your changes via `git diff` and scores them against an oracle patch using SWE-RL-style diff-similarity reward.