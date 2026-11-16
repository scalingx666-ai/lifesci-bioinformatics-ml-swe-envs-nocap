# Issue

**Title:** fix(rdkit): update fingerprint generation to use rdFingerprintGenerator API

## Description

- Replace direct calls to AllChem, Pairs, and Torsions with rdFingerprintGenerator in similarity_search.py
- Update example code in SKILL.md to reflect the new API usage
- Maintain existing functionality while adopting the modern fingerprint generation interface recommended by RDKit

## Task

Modify the repository so that the issue described above is resolved. The repository is checked out at base commit `a31cf4dd97e0`. Edit files in place; the verifier captures your changes via `git diff` and scores them against an oracle patch using SWE-RL-style diff-similarity reward.