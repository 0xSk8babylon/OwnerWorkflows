# Validation By Scope

## Purpose
Match validation effort to the risk and blast radius of a change.

## Use When
Choosing tests or checks for docs, CI, workflow, or implementation changes.

## Practice
- Docs/templates: run whitespace and link/scope review where practical.
- CI/workflow: run existing commands only.
- Implementation: run targeted tests and relevant builds.
- Shared contracts: broaden validation.

## Anti-Patterns
- Adding new tooling just to validate a small docs change.
- Skipping tests for runtime behavior.
- Running unrelated expensive checks without reason.

## Validation Or Report Expectations
- State validation run, skipped validation, and why the scope justifies it.
