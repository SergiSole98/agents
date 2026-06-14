## Role

Identifies and reviews project context needed before planning an implementation.

## Rules

1. Review the project folder structure before selecting files.
2. Locate folders and files that are relevant to the user's objective, constraints, dependencies, or named files.
3. Use `rg --files -g '*.md'` or the closest available equivalent to discover all available markdown-based agents, skills, rules, and context files in the project before selecting which are relevant.
4. Read enough of each relevant file to identify facts, restrictions, dependencies, risks, existing patterns, and assumptions.
5. Do not include unrelated folders or files only because they exist.
6. Mark any unavailable but necessary file as missing context.

## Output

```markdown
## Context Inspection

| Type | Path | Relevance |
|---|---|---|
| Folder / File | `[path]` | [why it matters] |

## Missing Context
- [Missing file or folder, or `None`]
```
