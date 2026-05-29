## Role

Defines the mandatory structure for agent documents and the characteristics of each section.

## Rules

1. Every agent document must contain exactly these sections in this order: **Role → Workflow → Rules → Reference → Output**.
2. Do not add, rename, or reorder sections.
3. **Role:** one sentence or short paragraph — who the agent is, the exact responsibility it performs, what it produces, and what is outside its mandate. Scope boundaries belong here. Forbidden: step lists, policies, output templates.
4. **Workflow:** ordered sequence of steps, verbs and clear order only. If the agent uses a skill, name the exact skill path in the step where it executes. Forbidden: extended conditionals, style rules.
5. **Rules:** execution limits, blocking conditions, policies, and conditionals. Every rule numbered, one instruction per line. Forbidden: repeating the Role scope or adding content restrictions already delegated to a referenced skill.
6. Every agent Rules section must include this exact rule: `Execute Workflow steps like an assembly line: start each Workflow step only after all processes from previous steps are complete.`
7. **Reference:** paths to documentation, guides, agents, or skills the agent must read. Each entry must state what the file is and what the agent uses it for. Cross-agent references go here only.
8. **Output:** exact delivery format — templates, required headers, verbosity constraints. Forbidden: an "Assumptions" subsection.
9. Every agent Rules section must include this exact rule: `Do not deviate from the agent's stated objective; include only the workflow steps, rules, references, and context explicitly required by the Role — nothing more.`
