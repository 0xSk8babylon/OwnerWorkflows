# Local Milestone Commit

## Purpose
Create a safe local commit for an approved milestone without pushing.

## Preconditions
- Commit is explicitly allowed.
- Push is not allowed.
- Scope is concrete.
- Verification route is declared.
- Working tree has been inspected.

## Procedure
1. Run `git status --short`.
2. Run `git diff --check`.
3. Run required validation.
4. Inspect changed files against approved scope.
5. Stage only approved files.
6. Run `git diff --cached --name-only`.
7. Stop if unexpected files are staged.
8. Run `git diff --cached --check`.
9. Run `git diff --cached --stat`.
10. Commit with a concise milestone message.
11. Record the commit hash.
12. Run `git status --short`.

## Stop Conditions
- Unexpected files are changed or staged.
- Validation fails.
- Commit permission is ambiguous.
- Staged diff exceeds scope.
- Commit would include secrets or `.env` files.

## Constraints
- Never push.
- Never stage unrelated changes.
- Never commit failed verification without a separate owner decision.

## Output Required
- Commit hash.
- Files committed.
- Verification performed.
- Final git status.
- Push status: not pushed.

## Cross-References
- `templates/milestone-commit.md`
- `templates/review-before-commit.md`
- `practices/commit-isolation.md`
- `practices/local-first-push-later.md`
