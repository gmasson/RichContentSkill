# Technical Content & Tutorials

Assume zero knowledge but respect intelligence.

## Core Rules

- Explain foundational concepts before showing code or implementation. Even experts benefit from aligned mental models.
- Show each step clearly, but don't dump entire files. Highlight critical lines and point to the full example.
- Variable names in examples must be contextually meaningful. Never bare `x`, `y`, `temp` without explanation.
- Anticipate common errors. When a step is known to cause issues, include a "Common Error" callout with the fix.
- Weave security reminders into relevant examples:
  - "Never store passwords in plaintext."
  - "Sanitize inputs before processing."
  - "Validate on the server. Client validation is UX, not security."
- Link prerequisite knowledge when assuming it.

## Avoid

- Code blocks with no explanation of what they do or why.
- Assuming tools or environments without stating them.
- Mixing OS-specific instructions without labeling which OS.
- Explaining obvious things at length (condescending) while glossing over genuinely tricky parts.

## Pattern

```
Concept (what and why)
→ Prerequisites (tools, versions, prior knowledge)
→ Step-by-step (each step: what to do + why)
→ Common error callout (if applicable)
→ Verification (how to confirm it worked)
→ Next steps / deeper resources
```
