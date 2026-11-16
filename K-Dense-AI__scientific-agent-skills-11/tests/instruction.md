# Issue

**Title:** refactor: replace manual argv parsing with argparse

## Description

## Summary

This PR refactors three client scripts to use Python's `argparse` module instead of manual `sys.argv` parsing, providing better user experience, error handling, and input validation.

## Changes

- **uniprot_client.py**: Convert to argparse with mutually exclusive groups
- **peds_client.py**: Convert to argparse with comprehensive help text
- **trademark_client.py**: Convert to argparse with proper error handling

## Improvements

✅ Replaced error-prone manual argument parsing with robust argparse
✅ Added mutually exclusive argument groups for better command structure
✅ Implemented comprehensive help text with examples for each command
✅ Added short and long argument options (e.g., `-s` and `--search`)
✅ Improved error handling with proper `parser.error()` calls
✅ Better input validation through argparse type checking
✅ Consistent error messages to stderr with proper exit codes

## Example Usage

### Before
```bash
python uniprot_client.py  # No help available
```

### After
```bash
python uniprot_client.py --help  # Full help with examples
python uniprot_client.py --search "insulin AND organism_name:human" --format json
python uniprot_client.py --get P01308 --format fasta
```

All files compile successfully and are ready to use once their respective dependencies are installed.

## Task

Modify the repository so that the issue described above is resolved. The repository is checked out at base commit `6ac2a15e3933`. Edit files in place; the verifier captures your changes via `git diff` and scores them against an oracle patch using SWE-RL-style diff-similarity reward.