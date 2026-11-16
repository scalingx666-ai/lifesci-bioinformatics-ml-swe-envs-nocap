# Issue

**Title:** Vector3 unary - operator for Python API

## Description

Fix for  . The respected bits just had to be commented out from the
.sip file:

<pre>
In [3]: print Vector3(1,1,1)
(1.000000 1.000000 1.000000)

In [4]: print -Vector3(1,1,1)
(-1.000000 -1.000000 -1.000000)
</pre>

## Task

Modify the repository so that the issue described above is resolved. The repository is checked out at base commit `4fdaca2af723`. Edit files in place; the verifier captures your changes via `git diff` and scores them against an oracle patch using SWE-RL-style diff-similarity reward.