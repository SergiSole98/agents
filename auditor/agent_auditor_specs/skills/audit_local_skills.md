## Role

Checks whether each local skill used or required by an audited agent exists and complies with the skill structure standard.

## Rules

1. Identify every local skill executed in the audited agent Workflow.
2. Identify every local skill required by the responsibility delegation audit.
3. Verify each identified local skill file exists under the audited agent's `skills/` folder.
4. Verify each identified local skill complies with `common/skill_structure/skill_skill_structure.md`.
5. Verify each identified local skill keeps only functional logic that belongs outside the main agent file.
6. Treat missing, mislocated, structurally invalid, or orchestration-heavy local skills as violations.
7. Treat an identified local skill as passing only when it is present, structurally valid, and aligned to its delegated responsibility.

## Reference

- **`common/skill_structure/skill_skill_structure.md`** - Skill structure standard used to validate local skill files.
- **`generator/agent_spec_generator/skills/classify_responsibilities.md`** - Responsibility classification standard used to verify skill responsibility boundaries.

## Output

```markdown
## Local Skill Audit Findings

| Skill path | Status | Required fix |
|---|---|---|
| [path] | Pass / Violation | [fix or None] |
```
