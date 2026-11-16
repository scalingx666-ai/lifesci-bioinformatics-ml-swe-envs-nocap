# Issue

**Title:** fix(simpy): report a non-UTF-8 resource CSV as unreadable, not as a bad integer

## Description

`skills/simpy/scripts/event_trace_summary.py`, in `_read_resource_csv`:

```python
    except ValueError as exc:
        raise CliError(f"resource CSV contains an invalid integer: {exc}") from exc
    except (OSError, UnicodeError, csv.Error) as exc:
        raise CliError(f"cannot read resource CSV {path.name}: {exc}") from exc
```

`UnicodeError` is a subclass of `ValueError`, so the first handler claims the decode failures the second one was written for. A resource CSV that is not valid UTF-8 is reported as a number-parsing problem:

```
$ python event_trace_summary.py bad.csv
event_trace_summary.py: error: resource CSV contains an invalid integer: 'utf-8' codec can't decode byte 0xe9 in position 55: invalid continuation byte
```

That sends the reader looking for a malformed `count` or `utilization` column when the actual problem is the file's encoding — the JSONL branch of the same script gets this right and says `cannot read trace ...`.

Swapping the two handlers is enough: `csv.Error` and `OSError` are not `ValueError` subclasses, so nothing else changes hands.

Listing `UnicodeError` next to `OSError` is the established convention here — 42 `try` blocks in the repository mention `UnicodeError`, and this is the only one with a bare `except ValueError` in front of it. `_read_trace`, 90 lines up in this same file, uses `except (OSError, UnicodeError)` with no `ValueError` handler, and `anonymize_dicom.py` writes the pair as `(UnicodeError, ValueError)` — `UnicodeError` first.

### Verification

Ran the real CLI against three CSVs (a Latin-1 byte in an event label, a non-numeric `count`, and a well-formed file):

| input | before | after |
|---|---|---|
| non-UTF-8 byte | `resource CSV contains an invalid integer: 'utf-8' codec can't decode byte 0xe9 …` | `cannot read resource CSV bad.csv: 'utf-8' codec can't decode byte 0xe9 …` |
| `count=notanint` | `resource CSV contains an invalid integer: invalid literal for int() with base 10: 'notanint'` | unchanged |
| well-formed | summary JSON | unchanged |

🤖 Generated with [Claude Code](https://claude.com/claude-code)

## Task

Modify the repository so that the issue described above is resolved. The repository is checked out at base commit `1e5eeffbdad3`. Edit files in place; the verifier captures your changes via `git diff` and scores them against an oracle patch using SWE-RL-style diff-similarity reward.