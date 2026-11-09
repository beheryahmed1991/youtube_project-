# Project guidance

Build the YouTube clone described in the supplied Russian assignment (ТЗ).
Read docs/requirements.md, docs/status.md, and docs/architecture.md before work.

- Source material in the parent sources/ directory is read-only.
- All application code is AI-generated; preserve native project conversation records and the configuration used. Summaries do not replace those records.
- Never claim a requirement passes without observable evidence. Distinguish implemented, tested locally, and verified on clean Ubuntu.
- Work in small, reviewable changes. Preserve meaningful Git commits; do not squash or rewrite history for presentation.
- Do not commit credentials, personal data, or unrelated conversation histories. Use .env.example for configuration names.
- Enforce video permissions on the backend, including media and thumbnail access. UI hiding is insufficient.
- Prefer a modular application over unnecessary distributed services. Document consequential decisions and limitations.
- Add meaningful tests for critical access rules, video behavior, and the main user journey.
- Keep docs/status.md current after each milestone, including checks actually run and failures still open.
- Use subagents only when requested or explicitly assigned by project instructions. Give delegated tasks bounded scope and preserve their native records where available.
- Do not edit shared files concurrently. A single implementation owner integrates changes.
- Build, test, and deployment commands are not established yet. Add verified commands to README.md as they become available.

