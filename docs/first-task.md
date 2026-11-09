# First implementation task

## Role and context

You are the implementation owner for a recruitment assignment. Read AGENTS.md,
docs/requirements.md, docs/architecture.md, docs/evidence.md and docs/status.md.
The supervisor chat owns prioritization; the repository notes hold current decisions.
Do not modify the parent's read-only sources/ or AGENTS.md.

## Milestone 0 — Foundation

1. Verify an authentic way to retrieve native Codex project conversations,
   including any delegated sessions. Record the tested method and limitations.
   Do not invent an export or silently substitute Markdown summaries.
2. Inspect Git status and environment. Preserve existing files and commits.
3. Resolve Docker engine availability, reporting any required user action.
4. Establish the smallest FastAPI/PostgreSQL/frontend/worker Compose setup.
5. Add a migration mechanism, non-secret environment example, useful health
   checks and a documented startup command. Seed tooling must be repeatable.
6. Record commands actually run and results. Commit a logical verified foundation.

If native-session verification is blocked, continue reversible foundation work
only while preserving available records and clearly reporting the unresolved gate.

## Milestone 1 — Real video slice

Build registration/login and upload → processing → playback, with persistence,
upload/processing status, title/description and public/private access grants.
Validate a public browser playback/seek and an unauthorized private-media denial.
Add a minimal real-video demo fixture and focused tests against PostgreSQL.
Integrate early; avoid implementing all screens before this journey works.

## Report to supervisor

- Files/components changed and why.
- Exact checks run and outcomes, including deployment scope (local or clean Ubuntu).
- Requirement IDs covered, remaining limitations and blockers.
- Native history preservation status.
- Commit IDs and the next bounded task.

Do not label the submission ready based only on a local startup or a mocked UI.
