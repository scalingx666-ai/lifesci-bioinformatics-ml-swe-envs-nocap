# Issue

**Title:** fix: upgrade infographic review to Gemini 3.1 Pro and harden review failure handling

## Description

## Summary
- Switch infographic quality review model from `google/gemini-3-pro` to `google/gemini-3.1-pro-preview`
- Lower the `marketing` quality threshold from 8.5 to 8.0 to reduce unnecessary regeneration loops
- Treat review failures as `needs_improvement=True` with `score=None` instead of silently passing with a fabricated `7.5` score, so a broken review no longer short-circuits the iteration loop

## Test plan
- [ ] Run `generate_infographic_ai.py` end-to-end with a marketing prompt and confirm review uses Gemini 3.1 Pro
- [ ] Force a review failure (e.g. invalid API key for the review model) and confirm the loop continues to the next iteration instead of accepting the image
- [ ] Confirm score-based logging shows `✗ Review failed` when the review errors and `✓ Score: X/10` on success

🤖 Generated with [Claude Code](https://claude.com/claude-code)

## Task

Modify the repository so that the issue described above is resolved. The repository is checked out at base commit `33b69c5d58bc`. Edit files in place; the verifier captures your changes via `git diff` and scores them against an oracle patch using SWE-RL-style diff-similarity reward.