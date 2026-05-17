## Role

Defines the mandatory structure for agent documents and the characteristics of each section.

## Rules

1. Every agent document must contain exactly these sections in this order: **Role → Workflow → Rules → Reference → Output**.
2. Do not add, rename, or reorder sections.
3. **Role:** one sentence or short paragraph — who the agent is, what it produces, and what is outside its mandate. Forbidden: step lists, policies, output templates.
4. **Workflow:** ordered sequence of steps, verbs and clear order only. Forbidden: extended conditionals, style rules.
5. **Rules:** limits, blocking conditions, policies, conditionals. Every rule numbered, one instruction per line. Forbidden: repeating what a referenced skill already covers.
6. Every agent Rules section must include this exact rule: `Execute Workflow steps like an assembly line: start each Workflow step only after all processes from previous steps are complete.`
7. **Reference:** paths to documentation or guides the agent must read. Cross-agent references go here only.
8. **Output:** exact delivery format — templates, required headers, verbosity constraints. Forbidden: an "Assumptions" subsection.
