## Role

Writing guidelines for agent documents. For mandatory sections and their order, apply `common/agent_structure/skill_agent_structure.md`.

## Rules

### Role

1. One sentence or short paragraph: who the agent is, what it produces, and what is outside its mandate.
2. Forbidden: step lists, long policies, output templates, skill paths unless they define identity in one line.
3. Test: if it reads as "how to do it step by step" or "never do X," it does not belong in Role.

### Task

4. Ordered sequence of steps. Verbs and clear order only. One step per executable action.
5. Forbidden: long conditionals, repeated "do not / always," style rules — those belong in Rules.
6. Test: "Always happens in the flow?" → Task. "Exception or limit?" → Rules.

### Rules

7. Numbered, one instruction per line. No mixed-command paragraphs.
8. Forbidden: repeating word-for-word what is already in Reference — "apply [path]" is enough.
9. Each rule must prevent one concrete failure; otherwise delete it.
10. Do not repeat — verbatim or paraphrased — what a referenced skill already covers.

### Reference

11. Paths to documentation or guides the agent must read. Include only what is explicitly requested or essential.
12. Cross-agent references go here only — not in Role, Task, or Rules.

### Output

13. Exact delivery format: templates, required headers, verbosity constraints.
14. Forbidden: an "Assumptions" subsection inside Output.

## Reference

- **`common/agent_structure/skill_agent_structure.md`** - Mandatory sections, order, and characteristics.
