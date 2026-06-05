# Closeout Automation Run

Use this prompt to stabilize and report after a temporary automation run.

```text
Close out the active temporary automation run.

Before final response:

- run git status --short
- run git diff --check
- inspect changed files
- confirm changed files match approved scope
- report verification honestly
- report commit status
- report push status
- identify hard stops touched or avoided
- identify next safe boundary

Use this report format:

## Automation Report

### Summary

### Scope

### Files Changed

### API / Schema / Persistence Impact

### Verification

### Automated Approvals Made

### Hard Stop Review

### Git State

### Risks / Blockers

### Next Safe Boundary
```

## Guardrails
- Do not hide dirty state.
- Do not claim skipped verification.
- Do not push.
- Do not continue into a new scope during closeout.
