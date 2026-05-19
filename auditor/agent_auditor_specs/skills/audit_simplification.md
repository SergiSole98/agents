## Role

Applies simplification checks to an audited agent and its local skills.

## Rules

1. Apply `common/rules/skill_simplification_check.md` to the audited agent file.
2. Apply `common/rules/skill_simplification_check.md` to each local skill that the audited agent uses or the audit creates or updates.
3. Mark duplicated, unsupported, overlapping, or misplaced instructions as violations.
4. Move misplaced instructions to the section owned by the applicable structure standard.
5. Do not add new restrictions or strengthen existing ones when simplifying.

## Reference

- **`common/rules/skill_simplification_check.md`** - Simplification standard used to detect duplicated, unsupported, overlapping, or misplaced instructions.
- **`common/agent_structure/skill_agent_structure.md`** - Agent section ownership standard used for audited agent simplification.
- **`common/skill_structure/skill_skill_structure.md`** - Skill section ownership standard used for local skill simplification.

## Output

```markdown
## Simplification Findings

| File | Section | Finding | Required fix |
|---|---|---|---|
| [path] | [section] | [finding] | [fix] |
```
