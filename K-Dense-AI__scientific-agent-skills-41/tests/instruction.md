# Issue

**Title:** Sync writing skills from claude-scientific-writer

## Description

## Summary

- Synced writing skill content from the claude-scientific-writer repository to ensure both repos have the superset of content
- Updated latex-posters/SKILL.md with expanded poster generation guidelines and mandatory pre-generation review steps
- Enhanced research-lookup/SKILL.md with improved output options and error handling
- Added criteria for identifying high-quality literature and influential papers
- Revised abstract writing instructions for flowing paragraphs over structured formats
- Included best practices for AI schematic generation regarding figure numbering and content clarity

## Files Changed

- `hypothesis-generation/references/literature_search_strategies.md`
- `latex-posters/SKILL.md` (major update)
- `literature-review/references/database_strategies.md`
- `markitdown/assets/example_usage.md`
- `research-lookup/SKILL.md` (major update)
- `scientific-schematics/references/best_practices.md`
- `scientific-schematics/scripts/generate_schematic_ai.py`
- `scientific-writing/references/imrad_structure.md`

## Test plan

- [ ] Verify skill documentation renders correctly
- [ ] Test latex-posters skill with sample poster generation
- [ ] Test research-lookup skill functionality

Made with [Cursor](https://cursor.com)

## Task

Modify the repository so that the issue described above is resolved. The repository is checked out at base commit `49024095e304`. Edit files in place; the verifier captures your changes via `git diff` and scores them against an oracle patch using SWE-RL-style diff-similarity reward.