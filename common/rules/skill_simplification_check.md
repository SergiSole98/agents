## Role

Checks whether document sections can be simplified by removing duplication, unsupported inference, or responsibilities placed in the wrong structural layer.

## Rules

1. Read the target document's Role, Workflow, Rules, Reference, and Output sections when they exist.
2. Read the applicable structure standard before deciding which section owns a responsibility.
3. Use `common/agent_structure/skill_agent_structure.md` as the source of truth for agent section ownership.
4. Use `common/skill_structure/skill_skill_structure.md` as the source of truth for skill section ownership.
5. Use `generator/agent_spec_generator/skills/classify_responsibilities.md` to decide the agent-versus-local-skill boundary, and prefer an existing owner over a new skill when the boundary allows either.
6. Check whether any instruction in Role, Workflow, Rules, Reference, or Output duplicates an instruction in another section.
7. Check whether each rule duplicates another rule in the same Rules section.
8. Treat content as duplicated when it restates the same instruction verbatim or paraphrased, even with different wording.
9. If two or more instructions overlap partially, replace them with a single merged instruction in the section that owns the responsibility.
10. Remove unsupported inferred rules when they are not directly supported by the user request, the approved plan, or a reviewed reference file.
11. Simplify by first deleting redundant content, then merging overlapping content, then moving it to an existing owner section or skill; create a new skill only as a last resort.
12. Move a responsibility placed in the wrong section to the section owned by the applicable structure standard.
13. Move an agent responsibility that belongs in a local skill to its existing owner skill according to the responsibility classification standard, and create a new skill only when no existing skill can own it.
14. When applying a correction, do not add new restrictions or strengthen existing ones; apply the smallest change that fixes the concrete defect.
15. For each simplification applied, record the section name, item number when available, defect type, and one-line explanation.

## Reference

- **`common/agent_structure/skill_agent_structure.md`** - Agent section ownership standard used to decide whether agent content belongs in Role, Workflow, Rules, Reference, or Output.
- **`common/skill_structure/skill_skill_structure.md`** - Skill section ownership standard used to decide whether skill content belongs in Role, Rules, Reference, or Output.
- **`generator/agent_spec_generator/skills/classify_responsibilities.md`** - Responsibility boundary standard used to decide whether agent content belongs in the main agent or a local skill.
