# Submission evidence workflow

## Current state

Native conversation export/retrieval for this Codex desktop setup is NOT VERIFIED.
The brief names several tools, but does not explicitly give a Codex desktop
export procedure. Verify an authentic retrieval route and, if necessary, ask
the recruiter whether that native format is acceptable before relying on it.

## Before substantial implementation

1. Identify the actual tool/version used and where original project session records are stored or exported.
2. Test retrieval of a short project session; inspect that prompts, responses and relevant tool activity are present.
3. Determine whether delegated sessions require separate collection. Verify rather than assume.
4. Inventory only the project-relevant instructions, skills, agents, settings and integrations actually used.
5. Keep unrelated conversations and live secrets out of project prompts and configuration files from the beginning.

## During development

- Preserve original session files and tool-generated exports without rewriting them.
- Keep a manifest mapping sessions to milestones and configuration snapshots.
- Use focused commits that reflect actual work; preserve failed approaches when they explain decisions.
- Keep secrets in local environment configuration, with non-secret examples in Git.
- Record test/deployment outcomes, limitations and known failures truthfully.

## Packaging gate

- Complete application repository including hidden .git directory and commits.
- README, architecture/decision notes, tests and demo seed tooling.
- Native supervisor, implementation and review conversations relevant to the task.
- Actual configuration used, with an inventory and any necessary disclosure of omissions.
- Scan for secrets. If a required original artifact contains a secret, rotate it
  and agree a handling approach; do not silently alter it and call it original.
- Extract the final archive into a new directory and verify its contents.
- Rehearse deployment on a clean Ubuntu VM. Local Windows checks alone do not satisfy that requirement.

