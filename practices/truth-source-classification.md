# Truth Source Classification

## Purpose
Classify evidence before deciding whether to change docs, doctrine, tests, or implementation.

## Use When
Sources disagree or a decision depends on intended behavior, current behavior, verified behavior, or product meaning.

## Practice
- Owner intent: authoritative product meaning or desired direction.
- Doctrine truth: approved governance, architecture, boundary, and authority language.
- Code truth: what the current implementation actually does.
- Test truth: what behavior is verified or protected.
- Documentation truth: what docs claim or teach.
- Runtime behavior: observed behavior in the running system.
- Conflict cases: sources actively disagree.
- Gaps: a needed truth source is missing.
- Drift: source behavior or wording changed away from intent or doctrine.
- Intentional evolution: an approved change in meaning, behavior, or phase.
- Stop and report before routing when the classification is ambiguous or would change doctrine, architecture meaning, code, tests, remotes, or publication state.

## Anti-Patterns
- Letting one source silently overrule all others.
- Treating missing tests as proof of intended behavior.
- Treating docs as implementation approval.
- Treating code behavior as doctrine.

## Validation Or Report Expectations
- Report the question, source types inspected, agreement/conflict/gap/drift/evolution finding, and recommended route.
