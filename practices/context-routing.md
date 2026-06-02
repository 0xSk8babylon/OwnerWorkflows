# Context Routing

## Purpose
Reduce token load by loading the smallest useful context first.

## Use When
Starting a session, choosing an agent/skill/template, or navigating a large repo.

## Practice
- Read navigation or index files first.
- Load one relevant file before loading a folder.
- Follow references only when needed.
- Prefer summaries over bulk loading.

## Anti-Patterns
- Reading the whole repo before classifying the task.
- Loading every agent, skill, or template.
- Chasing references unrelated to the active milestone.

## Validation Or Report Expectations
- Report which file was loaded first and why, plus any follow-up context used.
