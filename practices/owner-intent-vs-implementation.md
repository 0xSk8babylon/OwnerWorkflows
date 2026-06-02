# Owner Intent vs Implementation

## Purpose
Keep product meaning aligned with owner intent while preserving facts about current runtime behavior.

## Use When
Owner language, docs, tests, or code appear to disagree about what the product should mean or currently does.

## Practice
- Owner intent is authoritative for product meaning.
- Implementation should obey product meaning, not casually redefine it.
- Code is authoritative for current runtime behavior.
- If owner intent and code behavior diverge, classify the divergence before changing either one.

## Anti-Patterns
- Treating accidental code behavior as product strategy.
- Editing doctrine to justify an implementation mismatch.
- Changing code before confirming whether the mismatch is a bug, gap, drift, or intentional evolution.

## Validation Or Report Expectations
- Report owner intent, current behavior, evidence inspected, divergence classification, and recommended route.
