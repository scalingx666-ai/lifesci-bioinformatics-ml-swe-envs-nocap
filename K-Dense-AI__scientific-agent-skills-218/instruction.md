# Issue

**Title:** Add community health files

## Description

Completes the three GitHub Community Standards items the repository was missing. `gh api repos/K-Dense-AI/scientific-agent-skills/community/profile` currently reports `health_percentage: 75` with `code_of_conduct`, `issue_template`, and `pull_request_template` all `null`.

## What's here

**`CODE_OF_CONDUCT.md`** — Contributor Covenant 2.1, unmodified except for the enforcement contact (`contact@k-dense.ai`) and a note directing security vulnerabilities to `SECURITY.md` rather than the conduct address.

**`.github/ISSUE_TEMPLATE/`** — three YAML issue forms and a config:

| Template | Labels | Purpose |
|---|---|---|
| `bug_report.yml` | `bug`, `needs-triage` | Wrong output, broken script, failing install, instructions an agent can't follow. Collects agent host + model, since skill behavior varies by host. |
| `new_skill_request.yml` | `enhancement`, `skill-request`, `needs-triage` | Asks for the "what it does" and "when to use it" halves of a skill description, plus official docs and credential requirements. |
| `skill_improvement.yml` | `enhancement`, `needs-triage` | Stale APIs, thin examples, descriptions that trigger at the wrong time. |

`config.yml` sets `blank_issues_enabled: false` and adds contact links to private vulnerability reporting, `CONTRIBUTING.md`, the Agent Skills specification, and the K-Dense docs. Discussions are disabled on this repository, so nothing links there.

**`.github/PULL_REQUEST_TEMPLATE.md`** — summary, type of change, skills touched, how it was tested, and a checklist grouped into skill format / validation and tests / content and safety. The checklist items are taken from the existing Pull Request Checklist in `CONTRIBUTING.md` rather than invented, so there is one source of truth to keep in sync.

**`CONTRIBUTING.md`** — one added line linking the Code of Conduct.

## Notes

- Two labels referenced by the templates did not exist and were created ahead of this PR: `needs-triage` (`#ededed`) and `skill-request` (`#1d76db`). All other labels used were already present.
- All four YAML files parse and conform to GitHub's issue-form schema (validated locally: allowed `type` values, `id`/`label` present on every non-markdown block, non-empty `options` on every dropdown).
- Nothing under `skills/` is touched, so the skill-spec and PR-scan workflows have no work to do here.
- The `health_percentage` will not move until this merges to `main`.

## Task

Modify the repository so that the issue described above is resolved. The repository is checked out at base commit `752753bf7214`. Edit files in place; the verifier captures your changes via `git diff` and scores them against an oracle patch using SWE-RL-style diff-similarity reward.