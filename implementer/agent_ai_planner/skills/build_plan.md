## Role

Builds the final implementation plan from the validated hypothesis, reviewed context, and selected capabilities.

## Rules

1. Build the final plan only after the main hypothesis has been validated against the reviewed files and context.
2. If the main hypothesis cannot be fully validated, mark the plan as `parcialmente validado` and state the remaining uncertainty.
3. If information is missing but the plan can still advance partially, mark the plan as `parcialmente validado` and state what remains uncertain.
4. Infer success criteria from the objective and context; do not ask a separate criteria question.
5. Keep the final plan short, practical, and decision-first.
6. Write the final plan in Spanish.
7. Deliver a `Plan final`, not a brief.
8. Identify only the required files expected to be modified, what will be modified in each file, and why each change is needed.
9. Do not list optional files, recommended documentation updates, or files that were only reviewed.
10. Include a separate capabilities section for the implementer with only selected agents and skills, or state that none should be activated.
11. Do not output a full step-by-step implementation plan.
12. Do not list read, inspect, synthesis, or validation steps unless they change which files will be modified.
13. Every required file expected to be modified must appear explicitly with its full relative path.
14. For every required file expected to be modified, state the exact section, function, block, or lines to change when known, what will change there, and why that change is needed.
15. If a file could not be reviewed, do not invent exact changes. Use `Pendiente de confirmar tras revisar [archivo]`.
16. Do not include sections for objective, context, reviewed files, hypothesis, success criteria, validation, risks, or optional recommendations.
17. Do not include an explicit user acceptance question before implementation.
18. When the plan creates or modifies an agent, apply `../../../generator/agent_spec_generator/skills/classify_responsibilities.md` before selecting its required files.
19. Use the responsibility classification as the source of truth for the planned main-agent boundary and required local skills.
20. List the main agent file and every local skill required by the responsibility classification as separate mandatory files.
21. Keep the planned main agent change limited to orchestration, skill calls, blocking conditions, references, quality gates, and output routing.
22. Map every planned business logic, domain logic, content generation, interpretation, transformation, evaluation, validation, or reusable reasoning responsibility to an explicit local skill file.
23. When the plan creates an agent, include its mandatory local `skills/quality_audit.md` as a required file.
24. Do not state `No activar capacidades adicionales.` when the plan creates or modifies an agent; include the agent-spec generator and agent auditor.

## Reference

- **`../../../generator/agent_spec_generator/skills/classify_responsibilities.md`** - Responsibility classifier used to determine the planned main-agent boundary and required local skills.
- **`../../../generator/agent_spec_generator/agent_spec_generator.md`** - Agent generation standard used to determine mandatory agent files and implementation capabilities.

## Output

```markdown
# Plan final

## Archivos que voy a modificar
| Archivo obligatorio | Qué modificaré | Por qué |
|---|---|---|
| `[ruta/archivoX.ext]` | [qué sección/regla/bloque se modificará y qué se cambiará] | [por qué hace falta este cambio] |
| `[ruta/archivoY.ext]` | [qué se modificará] | [por qué hace falta este cambio] |

Use this level of detail:
| `Agents/analysis_orchestrator.md` | Ajustar `Workflow`, `Rules`, `Reference` y `Output` para insertar `agent_news_events_analyst` después de confirmar `News/`, `Events/` y `Technical_analysis/`. | El orquestador debe producir primero el análisis combinado de noticias/eventos y luego pasarlo al flujo de análisis técnico/inversión. |
| `Agents/Invest_Analysis/News_Events/agent_news_events_analyst.md` | Crear el nuevo agent para leer `Analisis/<asset>/News/news.md` y `Analisis/<asset>/Events/events.md`, aplicar `Agents/Skills/news_interpreter.md` y escribir `Analisis/<asset>/News_events_analysis/news_events_analysis.md`. | Centraliza la interpretación de noticias/eventos antes de que otros agentes consuman esa señal. |

Do not include optional files such as `README.md` unless the user explicitly asks to update documentation.

## Capacidades a activar por el implementer
| Tipo | Ruta | Uso obligatorio |
|---|---|---|
| `skill` | `[ruta/skill.md]` | [cómo mejora esta implementación concreta] |
| `agent` | `[ruta/agent.md]` | [qué parte concreta debe delegar o consultar el implementer] |

If no additional capability is useful:

`No activar capacidades adicionales.`

## Implementacion
Delegar este plan a `agent_ai_implementer`.
```
