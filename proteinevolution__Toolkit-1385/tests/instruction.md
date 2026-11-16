# Issue

**Title:** Update macros to 2.5.6

## Description

Updates [com.softwaremill.macwire:macros](https://github.com/softwaremill/macwire) from 2.5.4 to 2.5.6.
[GitHub Release Notes](https://github.com/softwaremill/macwire/releases/tag/v2.5.6) - [Version Diff](https://github.com/softwaremill/macwire/compare/v2.5.4...v2.5.6)

I'll automatically update this PR to resolve conflicts as long as you don't change it yourself.

If you'd like to skip this version, you can just close this PR. If you have any feedback, just mention me in the comments below.

Configure Scala Steward for your repository with a [`.scala-steward.conf`](https://github.com/scala-steward-org/scala-steward/blob/97ef5956853b9dd4bc8469e71d9c6e077ad04f0a/docs/repo-specific-configuration.md) file.

Have a fantastic day writing Scala!

<details>
<summary>Files still referring to the old version number</summary>

The following files still refer to the old version number (2.5.4).
You might want to review and update them manually.
```
frontend/yarn.lock
```
</details>
<details>
<summary>Ignore future updates</summary>

Add this to your `.scala-steward.conf` file to ignore future updates of this dependency:
```
updates.ignore = [ { groupId = "com.softwaremill.macwire", artifactId = "macros" } ]
```
</details>

labels: test-library-update, early-semver-patch, semver-spec-patch, old-version-remains, commit-count:1

## Task

Modify the repository so that the issue described above is resolved. The repository is checked out at base commit `5d09e8bb769c`. Edit files in place; the verifier captures your changes via `git diff` and scores them against an oracle patch using SWE-RL-style diff-similarity reward.