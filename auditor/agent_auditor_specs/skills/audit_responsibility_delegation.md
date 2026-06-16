## Role

Classifies an audited agent's responsibilities and routes functional logic to an existing owner skill, recommending a new local skill only as a last resort.

## Rules

1. Classify every responsibility in the audited agent using `generator/agent_spec_generator/skills/classify_responsibilities.md`.
2. Keep main-agent responsibilities limited to workflow order, routing, file input and output, blocking conditions, references, and quality gates.
3. Classify business logic, domain logic, content generation, interpretation, transformation, evaluation, validation, and reusable reasoning as local-skill responsibilities.
4. Treat functional logic left in the audited agent Role, Workflow, Rules, Reference, or Output as a violation only when no existing skill already owns it.
5. Route each functional responsibility to its existing owner skill by modification when one already covers it.
6. Recommend a new local skill only when no existing skill can own the responsibility after modification, merge, or move.
7. Place every recommended new skill path under the audited agent's `skills/` folder.
8. Treat a required local skill that is not called in the audited agent Workflow as a violation.
9. Treat a required local skill that is not documented in the audited agent Reference as a violation.

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

| Skill path | Functional responsibility | Action | Requirements |
|---|---|---|---|
| `skills/[skill_name].md` | [responsibility] | Modify existing / New skill | [requirements] |
```
