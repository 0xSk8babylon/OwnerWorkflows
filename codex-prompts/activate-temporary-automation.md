# Activate Temporary Automation

Use this prompt when the owner wants Codex to automate routine safe work inside a bounded task, phase, or milestone.

```text
Activate Temporary Automation Orchestrator for:

- repo:
- branch:
- phase/task:
- allowed files/domains:
- forbidden actions:
- verification required:
- commit allowed:
- push allowed: no
- report required: yes

Before editing:

- inspect repo state
- identify current boundary
- report planned route
- stop if scope is unclear
```

## Guardrails
- Automation is inactive until explicitly activated.
- Push remains forbidden.
- Hard-stop actions stop the run instead of triggering in-run escalation.
- Final report is required.
