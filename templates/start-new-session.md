# Start New Session

## Context
- Repo path: `<repo-path>`
- Current branch expectation: `<branch>`
- Current goal: `<goal>`
- Known guardrails: `<guardrails>`

## Goal
Start a clean Codex session from verified repository state.

## Scope
Discovery, planning, and owner-approved work only.

## Guardrails
- Do not modify files until repo state and scope are confirmed.
- Do not push, delete branches, or rewrite history.
- Preserve existing dirty work unless owner approves changes.

## Steps
1. Run `pwd`.
2. Run `git status --short`.
3. Run `git branch --show-current`.
4. Run `git remote -v`.
5. Run `git log --oneline -5`.
6. Confirm current goal, allowed files, validation commands, and expected closeout.

## Validation
- Initial state reported before edits.
- Dirty files classified as in-scope, out-of-scope, or blocker.

## Output Required
- Current repo, branch, status, remotes, latest commits.
- Confirmed scope and guardrails.
- Next safe action.
