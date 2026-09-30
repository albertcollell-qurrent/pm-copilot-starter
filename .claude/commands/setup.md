---
description: Interview the PM and fill in the ground truth (context/ and CLAUDE.md placeholders)
---

You are setting up this PM copilot for its owner. Interview them, then write the ground truth.

1. Read `CLAUDE.md` and every file in `context/` to see what's still a `[PLACEHOLDER]`.
2. Interview the user **one question at a time**, 10 to 15 questions max. Cover: their name and role; the company and business model; the product and its main parts; users and buyers; key stakeholders and what each cares about; this quarter's goals; the meetings that fill their week; the PM tasks they most want to hand off; anything agents must never do. Skip what's already filled in.
3. Show a short summary of what you'll write and ask for corrections.
4. Write:
   - `context/company/overview.md`, `strategy.md`, `stakeholders.md`
   - `context/product/overview.md`, `users.md`, `glossary.md`
   - One `context/customers/{name}.md` per key customer mentioned (from `_template.md`)
   - Replace `[YOUR NAME]`, `[YOUR ROLE]`, `[YOUR COMPANY]` in `CLAUDE.md`
   - Rename `product-areas/example-area/` to their main area and fill in its `AGENT.md` if they gave enough detail
5. Anything you had to guess: write `[TO CONFIRM]`, never invent it.
6. Ask them to review the **Authority** section of `CLAUDE.md` and adjust it with them.
7. Finish by suggesting they add one real transcript to `research/` and run `/synthesize`.
