# Validate against plan

## Context
Use after implementing plan steps or before reporting completion.

## Rules
1. Validate each success criterion from the plan.
2. Run available checks that directly prove the implemented result.
3. If automated validation is unavailable, perform a concrete manual inspection.
4. Do not claim completion for an unchecked criterion.
5. Report validation gaps explicitly.
6. Tie every validation result to the relevant plan criterion.
7. Compare each plan step with the work actually performed.
8. If a plan step or criterion is not satisfied, return to implementation for that specific gap.
9. Repeat implementation and validation until all plan items pass or a blocker is found.
10. Do not produce a completion report while any non-blocked plan item remains incomplete.
