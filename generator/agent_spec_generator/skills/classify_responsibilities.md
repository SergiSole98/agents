## Role

Classifies requested agent responsibilities into main-agent workflow responsibilities and isolated local-skill functional logic before an agent is drafted.

## Rules

1. Keep the main agent classification limited to workflow order, routing, file input and output, blocking conditions, references, and quality gates.
2. Classify business logic, domain logic, content generation, interpretation, transformation, evaluation, validation, and reusable reasoning as local-skill responsibilities.
3. Remove every user-requested functional responsibility from the main agent file classification.
4. Decide whether the requested agent needs one or more separate local skills before drafting the main agent file.
5. Create a separate local skill recommendation for each coherent functional responsibility that can be isolated from orchestration.
6. Do not classify functional logic as an agent Rule unless it only defines a scope boundary or blocking condition.
7. Count the exact number of task-specific local skills required by the classification.
8. Place every recommended task-specific skill under the drafted agent's `skills/` folder.
9. State that no task-specific local skill is needed only when the request contains no functional responsibility.

## Reference

- **`../../../common/agent_structure/skill_agent_structure.md`** - Agent structure standard used to identify valid main-agent responsibilities.

## Output

```markdown
## Responsibility Classification

| Responsibility | Classification | Destination | Reason |
|---|---|---|---|
| [responsibility] | Main agent / Local skill | [agent file or skill path] | [short reason] |

## Skill Decision
[One sentence stating whether task-specific local skills are required.]

## Skill Count
[Number of task-specific local skills required.]

## Required Local Skills
| Skill path | Functional responsibility | Requirements to pass to skill generator |
|---|---|---|
| `skills/[skill_name].md` | [responsibility] | [requirements] |

## Main Agent Boundary
[One sentence describing what remains in the main agent file.]
```
