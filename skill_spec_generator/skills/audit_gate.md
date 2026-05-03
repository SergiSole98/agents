# Audit Gate Skill

## Rules

1. Draft the full spec according to the relevant standard (writing_agent_skill.md, writing_skill_skills.md, etc.).
2. Submit the draft to the designated auditor agent specified in task.
3. If auditor flags violations, apply all corrections immediately; do not deliver incomplete corrections.
4. If auditor confirms compliance, deliver the Output format as-is.
5. If original intent is ambiguous during rewrite, ask for clarification before proceeding.

## Reference

**Auditor Agents:**
- `../../agent_auditor_specs/agent_auditor_specs.md` - Audits generated specs for compliance.

**Standards to reference during draft:**
- `common/writing_agent_skill.md` - Agent structure.
- `writing_skill_skills.md` - Skill structure.
- `prompt_syntax.md` - Text formatting.
