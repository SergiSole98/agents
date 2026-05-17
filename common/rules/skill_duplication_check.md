## Role

Checks whether the rules of a document are duplicated internally or across referenced files, and whether any can be unified.

## Rules

1. Read the Rules section of the target document.
2. For each rule, check whether the same instruction already exists in another rule of the same document.
3. A rule is a duplication if it restates existing content verbatim or paraphrased, even with different wording.
4. If two or more rules overlap partially, flag them as candidates for unification and propose a single merged rule.
5. When proposing a correction, do not add new restrictions or strengthen existing ones; identify the concrete defect and propose the smallest change that fixes it.
6. Flag each duplication or unification candidate: rule numbers and one-line explanation.
