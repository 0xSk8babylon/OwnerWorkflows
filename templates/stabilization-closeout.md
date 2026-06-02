# Stabilization Closeout

## Context
- Repo path: `<repo-path>`
- Completed work: `<summary>`
- Validation target: `<validation>`

## Goal
End a session safely with verified state and a clear handoff.

## Scope
Closeout, validation, and continuity updates only when needed.

## Guardrails
- Approval gates apply at milestone boundaries, not every in-scope edit.
- "Safe to commit" and "safe to push" mean ready for owner review only.
- Do not push without owner approval.
- Do not hide dirty state.
- Do not create closeout commits for unrelated changes.

## Steps
1. Run `pwd`.
2. Run `git status --short`.
3. Run `git branch --show-current`.
4. Run `git log --oneline -5`.
5. Update continuity docs only if the repo uses them and the milestone requires it.
6. Run `git diff --check`.
7. Prepare a closeout summary or commit proposal.

## Validation
- `git diff --check`
- `<repo-specific validation>`

## Output Required
- Completed work.
- Final status.
- Validation performed.
- Deferred decisions.
- Recommended next action.
