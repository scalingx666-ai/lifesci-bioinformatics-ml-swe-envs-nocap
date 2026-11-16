# Issue

**Title:** Added Imaging Data Commons skill

## Description

Query and download public cancer imaging data from [NCI Imaging Data Commons](https://imaging.datacommons.cancer.gov) using [`idc-index`](https://github.com/ImagingDataCommons/idc-index) python package. Use for accessing large-scale radiology (CT, MR, PET) and pathology datasets for AI training or research. No authentication required. Query by metadata, visualize in browser, check licenses.

## Task

Modify the repository so that the issue described above is resolved. The repository is checked out at base commit `cd537c1af673`. Edit files in place; the verifier captures your changes via `git diff` and scores them against an oracle patch using SWE-RL-style diff-similarity reward.