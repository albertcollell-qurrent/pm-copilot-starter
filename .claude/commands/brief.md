---
description: Draft a Product Brief. Problem, metric, scope, boundaries. Never the solution
argument-hint: [area] [problem name]
---

1. Check for an opportunity assessment in `product-areas/{area}/discovery/opportunity-assessments/`. If none, stop and suggest `/discover` first (unless the user gives a reason it isn't needed).
2. Draft with `templates/product-brief-template.md`. Fill **Why** only. Fill **What** only if the user says the decision to build is made.
3. No solutions, user stories, flows, or technical approach. If you catch yourself writing "the system should...", reframe it as scope, a boundary, or an open question.
4. Save to `product-areas/{area}/briefs/{slug}.md` with Status `Why`.
5. Offer to run `/coach` on it.
