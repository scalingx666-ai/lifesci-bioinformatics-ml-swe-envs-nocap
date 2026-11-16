# Issue

**Title:** fix(rdkit): correct FractionCsp3 call and MolToSmarts parameter name

## Description

Lands the valid parts of #97 and #95, which target the pre-rename `scientific-skills/` path and cannot be merged directly.

## Changes

- `skills/rdkit/scripts/molecular_properties.py` — `Descriptors.FractionCsp3` → `Lipinski.FractionCSP3`
- `skills/rdkit/references/api_reference.md` — `isomericSmarts` → `isomericSmiles`

## Verification

Against RDKit 2026.03.3:

```
Descriptors.FractionCsp3(m)     FAIL -> AttributeError: module 'rdkit.Chem.Descriptors' has no attribute 'FractionCsp3'
Lipinski.FractionCSP3(m)        OK   -> 0.1111111111111111
Chem.MolToSmarts(m, isomericSmarts=False)  FAIL -> ArgumentError
Chem.MolToSmarts(m, isomericSmiles=False)  OK
```

This was a hard crash: `molecular_properties.py` failed for every input molecule on `main`. The script now runs end-to-end:

```
$ python3 skills/rdkit/scripts/molecular_properties.py "CC(=O)Oc1ccccc1C(=O)O"
  Fraction Csp3:       0.111
  QED Score:           0.550
  Lipinski Pass:       Yes
```

## Known remaining inaccuracy

The API reference documents `MolToSmarts(mol, isomericSmiles=False)`, but RDKit's actual default is `True`:

```
MolToSmarts( (Mol)mol [, (bool)isomericSmiles=True [, (int)rootedAtAtom=-1]]) -> str
```

Left as-is to keep this change scoped to the contributed fixes. Worth a follow-up.

Credit to @jiaodu1307.

## Task

Modify the repository so that the issue described above is resolved. The repository is checked out at base commit `fdee3698c28c`. Edit files in place; the verifier captures your changes via `git diff` and scores them against an oracle patch using SWE-RL-style diff-similarity reward.