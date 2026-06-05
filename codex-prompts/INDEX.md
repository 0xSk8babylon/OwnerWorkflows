# Codex Prompts Index

Load one prompt to start the requested workflow. Load skills only for procedural detail.

| File | Purpose | When to use | Avoid loading unless needed |
| --- | --- | --- | --- |
| `session-start.md` | Begin from verified local state. | New session or repo switch. | Skip after state is already confirmed. |
| `repo-stabilization.md` | Stabilize workflow without app changes. | CI, branch, remote, validation repair. | Skip for docs-only milestones. |
| `docs-only-pass.md` | Guide documentation-only edits. | README, governance, handoff, templates. | Skip for app code changes. |
| `implementation-boundary-pass.md` | Check whether scope crosses runtime boundaries. | Ambiguous requests or implementation risk. | Skip for simple git commands. |
| `session-closeout.md` | Close with status, validation, and next action. | End of task or pause point. | Skip before work is complete. |
| `activate-temporary-automation.md` | Activate owner-controlled temporary automation for a bounded run. | Owner wants routine safe automation. | Skip unless automation is explicit. |
| `save-temporary-automation-orchestrator.md` | Save the temporary automation pattern into a project or workflow repo. | Reusing this doctrine elsewhere. | Skip for ordinary implementation. |
| `closeout-automation-run.md` | Stabilize and report after an automation run. | Temporary automation is ending. | Skip during active work. |
| `send-automation-report.md` | Send an existing local report with existing email configuration. | Owner requests report email delivery. | Skip unless report artifact and subject are provided. |

Do not load all prompts as startup context.
