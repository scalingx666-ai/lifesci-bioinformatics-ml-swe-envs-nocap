# Issue

**Title:** Add open-notebook skill with comprehensive API documentation

## Description

# Summary

This PR adds a complete new skill for Open Notebook, an open-source self-hosted alternative to Google NotebookLM. The skill includes comprehensive documentation, API reference, configuration guides, practical examples, and test infrastructure. **Closes** 

# Key Changes

- **SKILL.md**: Main skill documentation covering overview, quick start, core features (notebooks, sources, notes, chat, search, podcasts, transformations), and practical code examples for common workflows
- **API Reference** (`references/api_reference.md`): Complete REST API documentation covering all 10+ endpoint categories (notebooks, sources, notes, chat, search, podcasts, transformations, models, credentials) with request/response examples
- **Configuration Guide** (`references/configuration.md`): Docker deployment instructions, environment variable reference, AI provider setup (OpenAI, Anthropic, Google, Ollama, etc.), and security configuration
- **Architecture Documentation** (`references/architecture.md`): System design overview, component descriptions (FastAPI, SurrealDB, LangChain, Esperanto), and data flow diagrams
- **Code Examples** (`references/examples.md`): Practical Python examples for complete research workflows, file uploads, podcast generation, and custom transformations
- **Test Suite** (`scripts/test_open_notebook_skill.py`): Comprehensive TDD tests validating skill structure, SKILL.md frontmatter, content completeness, and documentation quality
- **Interaction Scripts**: 
  - `notebook_management.py`: CRUD operations for notebooks
  - `source_ingestion.py`: Ingesting URLs, files, and text content
  - `chat_interaction.py`: Chat sessions, message execution, and knowledge base search
- **Marketplace Registration**: Added open-notebook to `.claude-plugin/marketplace.json` skill registry

# Notable Implementation Details

- Skill description emphasizes key differentiators: full REST API, 16+ AI provider support, multi-speaker podcasts, data privacy through self-hosting
- Documentation covers both UI and programmatic (REST API) usage patterns
- Examples demonstrate async processing patterns for long-running operations (source ingestion, podcast generation)
- Test suite validates both structural requirements (directories, files) and content quality (sections, examples, provider mentions)
- Configuration guide includes both Docker Compose setup and environment variable reference for flexible deployment

## Task

Modify the repository so that the issue described above is resolved. The repository is checked out at base commit `f7585b76246a`. Edit files in place; the verifier captures your changes via `git diff` and scores them against an oracle patch using SWE-RL-style diff-similarity reward.