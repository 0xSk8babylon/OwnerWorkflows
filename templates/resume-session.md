# Resume Session

## Context
- Repo path: `<repo-path>`
- Prior goal: `<goal>`
- Latest known commit: `<commit>`
- Current phase: `<phase>`
- Next target: `<next-target>`

## Goal
Resume work from current repository state, not stale chat memory.

## Scope
Continue only the owner-approved phase.

## Guardrails
- Do not assume previous dirty state is safe.
- Do not overwrite user changes.
- Do not push or commit without owner approval.

## Steps
1. Run `pwd`.
2. Run `git status --short`.
3. Run `git branch --show-current`.
4. Run `git log --oneline -5`.
5. Compare current state to latest known commit and completed milestones.
6. Identify dirty files and whether they block the next target.

## Validation
- Resume target matches current branch and repo state.
- Dirty-state handling is explicit.

## Output Required
- Completed milestones.
- Current dirty state.
- Next target.
- Blockers or owner decisions needed.
