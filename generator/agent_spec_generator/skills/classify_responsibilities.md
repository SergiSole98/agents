## Role

Classifies requested agent responsibilities into main-agent workflow responsibilities and local-skill functional logic, routing each functional responsibility to an existing owner before recommending a new local skill.

## Rules

1. Keep the main agent classification limited to workflow order, routing, file input and output, blocking conditions, references, and quality gates.
2. Classify business logic, domain logic, content generation, interpretation, transformation, evaluation, validation, and reusable reasoning as local-skill responsibilities.
3. Remove every user-requested functional responsibility from the main agent file classification.
4. For each functional responsibility, check whether an existing local skill already owns it before deciding its destination.
5. Route a functional responsibility to its existing owner skill by modification when one already covers it.
6. Recommend a new local skill only when no existing skill can own the responsibility after modification, merge, or move.
7. Do not classify functional logic as an agent Rule unless it only defines a scope boundary or blocking condition.
8. Count separately the local skills to modify and the new local skills required by the classification.
9. Place every recommended new local skill under the drafted agent's `skills/` folder.
10. State that no new task-specific local skill is needed when the request contains no functional responsibility or when existing skills already own every functional responsibility.

## Reference

- **`../../../common/agent_structure/skill_agent_structure.md`** - Agent structure standard used to identify valid main-agent responsibilities.

## Output

```markdown
## Responsibility Classification

| Responsibility | Classification | Destination | Action | Reason |
|---|---|---|---|---|
| [responsibility] | Main agent / Local skill | [agent file or skill path] | Modify existing / New skill | [short reason] |

## Skill Decision
[One sentence stating whether existing skills cover the responsibilities and whether any new local skill is required as last resort.]

## Skill Count
[Number of local skills to modify and number of new local skills required.]

## Required Local Skills
| Skill path | Functional responsibility | Action | Requirements to pass to skill generator |
|---|---|---|---|
| `skills/[skill_name].md` | [responsibility] | Modify existing / New skill | [requirements] |

## Main Agent Boundary
[One sentence describing what remains in the main agent file.]
```
