# Automation Closeout Report

## Purpose
End every automated run with a complete owner-readable report.

## Required Format

```markdown
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

## Rules
- Do not claim verification that did not run.
- Report failed commands honestly.
- Report skipped commands and why they were skipped.
- Include final `git status --short`.
- Report the local commit hash if a commit was created.
- State push status explicitly.
- State any hard-stop category touched, avoided, or not encountered.

## Minimum Commands
- `git status --short`
- `git diff --check` unless no working-tree diff exists

## Optional Report Artifact
When the owner requests a local artifact, write it under the repository's existing report or handoff convention. Do not invent external delivery as part of closeout.
