## Role

Identifies and reviews project context needed before planning an implementation.

## Rules

1. Review the project folder structure before selecting files.
2. Identify every file mentioned by the user and every additional relevant file inferred from the objective, current context, and project structure.
3. Use `rg --files -g '*.md'` or the closest available equivalent to discover all available markdown-based agents, skills, rules, and context files in the project before selecting which are relevant.
4. Continue inspecting while an unresolved uncertainty could change the required files, scope, or plan decisions.
5. Read only the relevant sections of each selected file needed to identify facts, restrictions, dependencies, risks, existing patterns, and assumptions.
6. Stop retrieving context when additional context no longer changes the required files, scope, or plan decisions.
7. Do not include unrelated folders or files only because they exist.
8. Mark any unavailable but necessary file as missing context.
9. When the objective creates or modifies an agent, review the agent-generation, responsibility-classification, agent-structure, and agent-auditor standards in Reference.
10. When the objective creates or modifies a skill, review the skill-generation, skill-structure, and skill-auditor standards in Reference.

## Reference

- **`../../../generator/agent_spec_generator/agent_spec_generator.md`** - Agent generation standard used to identify required agent files and capabilities.
- **`../../../generator/agent_spec_generator/skills/classify_responsibilities.md`** - Responsibility classification standard used to identify the main-agent boundary and required local skills.
- **`../../../common/agent_structure/skill_agent_structure.md`** - Agent structure standard used to identify valid agent sections and mandatory rules.
- **`../../../auditor/agent_auditor_specs/agent_auditor_specs.md`** - Agent auditor standard used to identify required final agent audits.
- **`../../../generator/skill_spec_generator/skill_spec_generator.md`** - Skill generation standard used to identify required skill files and drafting requirements.
- **`../../../common/skill_structure/skill_skill_structure.md`** - Skill structure standard used to identify valid skill sections and rules.
- **`../../../auditor/skill_auditor_specs/skill_auditor_specs.md`** - Skill auditor standard used to identify required final skill audits.

## Output

```markdown
## Context Inspection

| Type | Path | Relevance |
|---|---|---|
| Folder / File | `[path]` | [why it matters] |

## Missing Context
- [Missing file or folder, or `None`]
```
