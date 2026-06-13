# Claude Entrypoint

This file is the Claude and Claude Code entrypoint for OwnerWorkflows. Use it to discover the canonical shared workflow instructions, then route through the same machine-readable files used by other agent harnesses.

OwnerWorkflows is the workflow source of truth for owner-controlled agent execution. It is a reusable workflow library, not a single giant prompt.

## Required Startup Sequence

Claude and Claude Code must:

1. Read `CLAUDE.md`.
2. Read `AGENTS.md`.
3. Read `OWNERWORKFLOWS_INDEX.md`.
4. Read `OWNERWORKFLOWS_ROUTER.md`.
5. Classify the user request.
6. Select the minimum relevant workflow docs.
7. Execute only within the selected scope.
8. Validate.
9. Produce a final report.
10. Stop before hard-stop boundaries unless the owner explicitly approved that boundary.

## Claude-Specific Routing Rules

- Treat `AGENTS.md` as the canonical cross-agent entrypoint.
- Treat `OWNERWORKFLOWS_INDEX.md` as the machine-readable inventory.
- Treat `OWNERWORKFLOWS_ROUTER.md` as the task router.
- Do not load, merge, or apply the entire `templates/` folder by default.
- Do not load every agent, skill, practice, template, prompt, or checklist by default.
- Select the smallest safe workflow set for the current task.
- Default to read-only inspection when scope is uncertain.
- Existing docs are constraints, not creative source material.
- Do not rewrite doctrine unless explicitly asked by the owner.
- Do not invent unavailable agents, skills, practices, templates, or capabilities.

## Owner Hard Stops

Stop and report if the task requires crossing any of these boundaries:

- no git push unless explicitly approved by owner
- no migrations
- no auth, security, or permission changes
- no deleting files
- no doctrine rewrites
- no unrelated repos
- no external services or secrets
- no deploys
- no broad refactors
- no destructive commands

If another instruction conflicts with these hard stops, preserve the hard stop and report the conflict.
