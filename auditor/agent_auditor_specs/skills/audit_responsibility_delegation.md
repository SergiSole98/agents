## Role

Classifies an audited agent's responsibilities and identifies functional logic that must be moved from the main agent file into local skills.

## Rules

1. Classify every responsibility in the audited agent using `generator/agent_spec_generator/skills/classify_responsibilities.md`.
2. Keep main-agent responsibilities limited to workflow order, routing, file input and output, blocking conditions, references, and quality gates.
3. Classify business logic, domain logic, content generation, interpretation, transformation, evaluation, validation, and reusable reasoning as local-skill responsibilities.
4. Treat functional logic left in the audited agent Role, Workflow, Rules, Reference, or Output as a violation.
5. Recommend one local skill for each coherent functional responsibility that can be isolated from orchestration.
6. Place every recommended skill path under the audited agent's `skills/` folder.
7. Treat missing required local skill files as violations.
8. Treat required local skills that are not called in the audited agent Workflow as violations.
9. Treat required local skills that are not documented in the audited agent Reference as violations.

## Reference

- **`generator/agent_spec_generator/skills/classify_responsibilities.md`** - Responsibility classification standard used to separate orchestration from functional logic.
- **`generator/agent_spec_generator/agent_spec_generator.md`** - Agent generation standard used to require local-skill creation before final agent drafting.
- **`generator/skill_spec_generator/skill_spec_generator.md`** - Skill generation standard used to define missing local skill requirements.

## Output

```markdown
## Responsibility Delegation Audit

| Responsibility | Classification | Destination | Status | Required fix |
|---|---|---|---|---|
| [responsibility] | Main agent / Local skill | [agent file or skill path] | Pass / Violation | [fix or None] |

## Required Local Skills

| Skill path | Functional responsibility | Requirements |
|---|---|---|
| `skills/[skill_name].md` | [responsibility] | [requirements] |
```
