## Role

Activates only the agents and skills selected in an approved implementation plan after verifying them against the current project's markdown files.

## Rules

1. Read the approved plan's `Capacidades a activar por el implementer` section before executing implementation steps.
2. If the approved plan states `No activar capacidades adicionales`, record that no additional capability was activated and continue.
3. If the approved plan has no capability section, record that no additional capability was provided and continue.
4. Identify available markdown files with `rg --files -g '*.md'` or the closest available equivalent.
5. Classify markdown files as agent, skill, rule, reference, or context using their path, headers, stated role, and workflow or rules sections.
6. Verify every selected capability by opening its exact path before applying it.
7. Treat a file as a skill only when its role and rules describe reusable execution behavior.
8. Treat a file as an agent only when its role and workflow describe delegated responsibility.
9. Apply a selected skill only when its rules directly improve the approved implementation task.
10. Consult or delegate to a selected agent only for the exact responsibility stated in the approved plan.
11. Do not activate a discovered capability that was not selected in the approved plan.
12. Do not activate a selected capability when its reviewed content is unrelated to the approved implementation task.
13. If a selected capability conflicts with the approved plan, follow the approved plan and report the capability as skipped.
14. If a selected capability path is missing or cannot be classified, stop and report the capability as blocked.
15. Keep implementation scope bound to the approved plan while applying selected capabilities.
16. Record every selected capability as used, skipped, or blocked for the final report.

## Output

Add capability results to the final implementation report:

```markdown
### Capability Check
- `[path]` - [used / skipped / blocked] - [short reason]
```
