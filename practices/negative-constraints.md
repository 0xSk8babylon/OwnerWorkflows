# Negative Constraints

## Purpose
Make prohibited actions explicit so safe work can proceed inside boundaries.

## Use When
The task has risks around publishing, runtime behavior, secrets, doctrine, or destructive git.

## Practice
- State what must not change.
- State what is allowed inside scope.
- Use negative constraints to avoid scope creep, not to block ordinary edits.
- Stop when a prohibited action becomes necessary.

## Anti-Patterns
- Treating constraints as vague preferences.
- Asking approval for every tiny allowed edit.
- Ignoring a constraint because validation passed.

## Validation Or Report Expectations
- Report any constraint touched, avoided, or requiring owner approval.
