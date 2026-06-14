## Role

Guides the conceptual quality of agent and skill content so every instruction operates at the correct altitude: specific enough to constrain behavior, flexible enough to handle variation.

## Rules
1. Write instructions at the level of intent, not implementation detail. Do not hardcode logic that the model must derive from context.
2. Do not write instructions so vague that the model must guess what to do. Every rule must resolve to a single unambiguous action.
3. State what the agent or skill must do, not how the underlying model should think.
4. Use direct, declarative language. Omit qualifiers that weaken the instruction ("try to", "if possible", "generally").
5. Do not repeat a constraint already enforced by a referenced skill or rule file.
6. When a rule has exceptions, state the exception explicitly rather than leaving it implied.