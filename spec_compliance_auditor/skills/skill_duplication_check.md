## Context

Detects rules in an agent document that restate — verbatim or paraphrased — what a referenced skill already covers.

## Rules

1. Read every skill file listed in the agent's Rules or Reference sections.
2. For each rule in the agent, check whether the same instruction already exists in any of those skills.
3. A rule is a duplication if it restates the skill's content verbatim or paraphrased, even with different wording.
4. Flag each duplication: section, rule number, and one-line explanation.
5. "apply [path]" is always sufficient — never flag it as duplication.
