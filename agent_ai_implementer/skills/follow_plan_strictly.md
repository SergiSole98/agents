# Follow plan strictly

## Context
Use when the agent receives an approved plan and must preserve its scope, order, and intent.

## Rules
1. Treat the provided plan as the source of truth.
2. Preserve the order of plan steps unless the plan explicitly allows reordering.
3. Do not add implementation work that is not required by the plan.
4. Do not remove a plan step because it seems unnecessary.
5. If a step is ambiguous enough to change implementation behavior, stop and ask one concrete question.
6. If a step is impossible in the current context, stop and report the blocker.
