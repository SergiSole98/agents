## Role

Applies audit findings by rewriting the audited agent file and creating or updating required local skill files.

## Rules

1. Rewrite the audited agent file so it complies with `common/agent_structure/skill_agent_structure.md`.
2. Create or update every required or noncompliant local skill under the audited agent's `skills/` folder.
3. Draft or revise local skills according to `common/skill_structure/skill_skill_structure.md`.
4. Use `generator/skill_spec_generator/skill_spec_generator.md` requirements when drafting missing local skills.
5. Copy `generator/agent_spec_generator/skills/quality_audit.md` verbatim into the audited agent's `skills/quality_audit.md` when missing or different.
6. Ensure the audited agent Workflow calls every required local skill at the correct execution point.
7. Ensure the audited agent Reference documents every used skill with what it is and what the agent uses it for.
8. Preserve original intent and apply the smallest change that fixes each violation.

## Reference

- **`common/agent_structure/skill_agent_structure.md`** - Agent structure standard used to rewrite the audited agent.
- **`common/skill_structure/skill_skill_structure.md`** - Skill structure standard used to create or update local skills.
- **`generator/skill_spec_generator/skill_spec_generator.md`** - Skill generation standard used to draft required local skills.
- **`generator/agent_spec_generator/skills/quality_audit.md`** - Required quality audit skill template copied verbatim into audited agents.

## Output

```markdown
## Applied Fixes

| File | Change | Reason |
|---|---|---|
| [path] | [change] | [reason] |
```
