---
description: Frame an opportunity before building. Who has the problem, evidence, top 3 assumptions, how to validate
argument-hint: [area] "[opportunity question]"
---

1. Load context (per `CLAUDE.md`), `product-areas/{area}/AGENT.md`, the area and root `customer-insights.md`, and relevant `context/customers/` files.
2. Search `research/` for evidence on the question. Quote and link it.
3. Fill `templates/opportunity-assessment-template.md`: the problem, evidence table, size, the top 3 assumptions that must be true, and a validation method for the riskiest one with a stop condition.
4. Be honest about thin evidence. One customer saying it once is an anecdote; say so.
5. Save to `product-areas/{area}/discovery/opportunity-assessments/{slug}.md`.
