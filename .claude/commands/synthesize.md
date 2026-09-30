---
description: The operating loop. Turn meeting notes in research/ into action items, customer insights, and flags
---

1. Load `chief-of-staff/AGENT.md` for the mandate and authority boundaries.
2. Find unsynthesized notes: every `research/**/*.md` (except README) not yet listed in `chief-of-staff/synthesis-log.md`. If $ARGUMENTS names a file, process just that one.
3. For each note:
   - **Action items** → append rows to `actions/tracker.md`: next `#`, one action per row, Owner, Source (link to the note), Due as an absolute date (`TBD` if not said), Status `Open`. Skip duplicates of open items.
   - **Customer/product signal** → add to the area's `discovery/customer-insights.md` (or root `discovery/customer-insights.md` if cross-area), under an existing theme when it fits or a new theme when it doesn't. Cite who said it, when, and link the note. Update the source count on the theme.
   - **Decision-worthy?** (affects multiple teams, hard to reverse, future teammates need the why) → do NOT write to `decisions/`. List it under "Flagged".
   - **Customer or stakeholder status change?** → do NOT edit `context/`. Propose the exact edit under "Flagged".
4. Prepend one entry to `chief-of-staff/synthesis-log.md`: processed, filed (with tracker #s and themes), flagged.
5. Reply with: what was filed (brief), then **Flagged for you** as a list, each with a suggested next step (`/decision ...`, or "approve this context edit?").
