# Issue

**Title:** feat: add Exa AI-powered search tool

## Description

## Summary

- Adds a new `exa-search` skill sibling to the existing `parallel-web` skill, under `scientific-skills/exa-search/`.
- Covers three capabilities via the Exa Python SDK (`exa-py`): **web search** (neural/auto/fast retrieval with content + filters), **URL extraction** (`/contents` batch extraction with text / highlights / LLM summary), and **find-similar** (surface pages related to a seed URL via Exa's embeddings — strong for "more papers like this one" or "competitors of this company" queries).
- Academic source strategy is built in: `category="research paper"` biases Exa's neural retrieval toward scholarly content, and the reference docs include a two-pass pattern combining a scholarly domain allowlist with an unrestricted pass.
- Scripts use PEP 723 inline dependency metadata, so `uv run --with exa-py python scripts/exa_search.py …` works without a separate install step. Auth via `EXA_API_KEY`.
- Adds one entry to `docs/scientific-skills.md` under **Web Search & Information Retrieval**, matching the Paperzilla precedent (#131).

## Usage example

```bash
export EXA_API_KEY=...

# Neural search biased toward scholarly sources, with highlights
uv run --with exa-py python scripts/exa_search.py \
  "alternatives to attention in sequence models" \
  --category "research paper" \
  --include-domains "arxiv.org,nature.com,openreview.net" \
  --num-results 10 \
  --highlights \
  -o attention-alternatives.json

# Batch-extract multiple URLs with focused summaries
uv run --with exa-py python scripts/exa_extract.py \
  https://arxiv.org/abs/2401.04088 \
  https://www.nature.com/articles/s41586-024-07566-y \
  --text --summary "methods and key findings" \
  -o extracted.json

# Find papers similar to a seed paper, excluding the same domain
uv run --with exa-py python scripts/exa_find_similar.py \
  https://arxiv.org/abs/2401.04088 \
  --category "research paper" \
  --exclude-source-domain \
  --num-results 15 \
  --highlights \
  -o similar-papers.json
```

## Files changed

- `scientific-skills/exa-search/SKILL.md` — routing table, decision guide, setup, academic source priority
- `scientific-skills/exa-search/references/web-search.md` — search reference including two-pass academic pattern
- `scientific-skills/exa-search/references/web-extract.md` — `/contents` reference for single or batch URL extraction
- `scientific-skills/exa-search/references/find-similar.md` — find-similar reference with refinement options
- `scientific-skills/exa-search/scripts/exa_search.py` — CLI wrapper around `client.search_and_contents`
- `scientific-skills/exa-search/scripts/exa_extract.py` — CLI wrapper around `client.get_contents`
- `scientific-skills/exa-search/scripts/exa_find_similar.py` — CLI wrapper around `client.find_similar_and_contents`
- `scientific-skills/exa-search/tests/test_exa_search.py` — stdlib `unittest` suite, 21 tests, no new dependencies
- `docs/scientific-skills.md` — add `Exa Search` entry under **Web Search & Information Retrieval**

## Design notes

- **Typed result models.** Each script defines a `@dataclass` for the API response shape (`SearchResult`, `ExtractedDocument`, `SimilarResult`) rather than dumping raw SDK objects, so the JSON output is stable and easy for downstream skills to parse.
- **Content fallback is explicit.** The `_build_contents` helper produces the right request body for any combination of `--text`, `--highlights`, `--summary`, and the result-typing code degrades gracefully when a response lacks one of those fields.
- **Integration attribution.** Each script sets `client.headers["x-exa-integration"] = "scientific-agent-skills"` so Exa can attribute API usage to this skill.
- **No new repo-level dependencies.** Script deps are declared inline via PEP 723; tests use only `unittest` + `unittest.mock` from stdlib.

## Test plan

- [x] Scripts pass `python -m py_compile` and `--help` runs cleanly
- [x] Unit tests pass locally: `python -m unittest discover -s scientific-skills/exa-search/tests -v` → **21/21 passing**
- [x] Tests mock `exa_py.Exa` so they never hit the live API
- [ ] Smoke-test against the real Exa API with a valid `EXA_API_KEY` (reviewer step if desired)
- [ ] Optional: run `skill-scanner scan scientific-skills/exa-search --use-behavioral` per the repo's security guidance

## Draft status

Opening as a **draft** to leave room for review and iteration before it lands. Happy to adjust structure, naming, or scope based on maintainer feedback.

## Task

Modify the repository so that the issue described above is resolved. The repository is checked out at base commit `25e1c0f5696f`. Edit files in place; the verifier captures your changes via `git diff` and scores them against an oracle patch using SWE-RL-style diff-similarity reward.