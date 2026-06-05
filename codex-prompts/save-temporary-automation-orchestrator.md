# Save Temporary Automation Orchestrator

Use this prompt to save the temporary automation pattern into a project or workflow repo.

```text
Add reusable owner-controlled temporary automation workflow docs.

Requirements:

- Inspect repo tree and indexes first.
- Do not duplicate equivalent existing doctrine.
- Add only missing reusable pieces.
- Keep content generic and project-neutral.
- Do not include private project history.
- Do not add secrets, providers, app code, migrations, or external setup.
- Use existing prompt/docs folder conventions.
- Update relevant navigation and indexes only.
- Run docs-only verification.
- Do not commit or push unless separately approved.

Core doctrine:

- inactive by default
- owner-activated only
- scope-bound at activation time
- additive-only by default
- no authority escalation
- hard stops for dangerous actions
- required final report
- no push unless separately approved
- no background promises
```

## Expected Output
- Summary.
- Files added.
- Files updated.
- Overlap avoided.
- Verification.
- Final git status.
- Recommended commit message.
