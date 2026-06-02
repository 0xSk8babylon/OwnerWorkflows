# Codex Prompts Index

Load one prompt to start the requested workflow. Load skills only for procedural detail.

| File | Purpose | When to use | Avoid loading unless needed |
| --- | --- | --- | --- |
| `session-start.md` | Begin from verified local state. | New session or repo switch. | Skip after state is already confirmed. |
| `repo-stabilization.md` | Stabilize workflow without app changes. | CI, branch, remote, validation repair. | Skip for docs-only milestones. |
| `docs-only-pass.md` | Guide documentation-only edits. | README, governance, handoff, templates. | Skip for app code changes. |
| `implementation-boundary-pass.md` | Check whether scope crosses runtime boundaries. | Ambiguous requests or implementation risk. | Skip for simple git commands. |
| `session-closeout.md` | Close with status, validation, and next action. | End of task or pause point. | Skip before work is complete. |

Do not load all prompts as startup context.
