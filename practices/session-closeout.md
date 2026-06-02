# Session Closeout

## Purpose
End work with clean state, validation, and a useful handoff.

## Use When
Completing, pausing, or handing off a session.

## Practice
- Check branch, status, remotes, and latest commits.
- Run validation appropriate to the scope.
- Report changed or committed files.
- Name deferred decisions and next safe action.

## Anti-Patterns
- Hiding dirty state.
- Reporting success without validation.
- Pushing as part of closeout without separate approval.

## Validation Or Report Expectations
- Include `git status --short`, validation results, risks, and whether commit/push readiness is only owner-review readiness.
