## Context

Fixed structure for agent documents. One file = one agent. Sections have fixed purposes; do not mix content across them.

## Rules

1. Every agent document must contain exactly these sections in this order: **Role → Task → Context → Rules → Reference → Output**.
2. Do not add, rename, or reorder sections.
3. **Role:** one sentence or short paragraph — who the agent is, what it produces, and what is outside its mandate. Forbidden: step lists, policies, output templates.
4. **Task:** ordered sequence of 3–7 steps, verbs and clear order only. Forbidden: extended conditionals, style rules.
5. **Context:** describes where the agent operates (meta vs domain), what the user is assumed to know, and what it will not do. Forbidden: imperative policy commands — move those to Rules.
6. **Rules:** limits, blocking conditions, policies, conditionals. Every rule numbered, one instruction per line. Forbidden: repeating what a referenced skill already covers.
7. **Reference:** paths to documentation or guides the agent must read. Cross-agent references go here only.
8. **Output:** exact delivery format — templates, required headers, verbosity constraints. Forbidden: an "Assumptions" subsection.
