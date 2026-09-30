# PM Copilot Starter

A starter kit for running product management as an **orchestrator** instead of an IC: a git repo of plain markdown that Claude Code reads before every task, a few agents that do IC-level PM work, and explicit rules for what they may do alone.

It comes from the talk *From IC to Orchestrator*. It's the smallest version of the system from that talk, stripped of company specifics so you can make it yours.

## The idea in one picture

```
Stakeholders ──► Meetings (Granola / transcripts) ──┐
                                                    ├──► PM Copilot (this repo) ──flags──► You
Docs (Drive / Notion / specs) ──────────────────────┘        ▲                              │
                                                             └────────decisions, context────┘
        ◄──────────── action items, recaps, briefs, decisions go back out ─────────────┘
```

Three layers:

| Layer | Folder | What it holds |
| --- | --- | --- |
| Ground truth | `context/` | Company, product, users, glossary, customers, market. Read first, every time. |
| Instructions | `CLAUDE.md`, `.claude/`, `*/AGENT.md` | Who each agent is, what it reads, what it may do alone, what it must bring to you. |
| Live work | `actions/`, `discovery/`, `decisions/`, `product-areas/`, `strategy/` | The output. Each run feeds the next one. |

## Quickstart (30 minutes)

1. **Get the repo.** Click "Use this template" (or clone it), then `cd` into the folder.
2. **Open Claude Code** in the folder: `claude`
3. **Run `/setup`.** Claude interviews you (company, product, users, stakeholders, where your week goes) and fills in `context/` and the `[BRACKETED]` placeholders in `CLAUDE.md`.
4. **Try the loop.** Drop a real meeting transcript into `research/` (or use the fictional example already there), then run `/synthesize`. You should see action items with owners and due dates land in `actions/tracker.md`, customer signals land in `discovery/customer-insights.md`, and anything decision-worthy flagged to you rather than written down.
5. **Fix what was wrong.** Tell Claude what it got wrong and have it update `CLAUDE.md` or the command. This is the real work: context is the product.

## Commands

| Command | What it does |
| --- | --- |
| `/setup` | Interviews you and fills in the ground truth. Run once, then re-run to refresh. |
| `/synthesize` | The operating loop: turns meeting notes in `research/` into action items, insights, and flags. |
| `/discover [area] "[question]"` | Frames an opportunity: who has the problem, evidence, top 3 assumptions, how to validate. |
| `/brief [area] [problem]` | Drafts a Product Brief (problem, metric, scope, boundaries), never the solution. |
| `/decision [title]` | Logs a decision with its rationale. |
| `/coach [file or question]` | Pressure-tests a doc or decision using the `product-coach` agent. |
| `/weekly` | Rolls up the week: what moved, what's stuck, what needs you. |
| `/granola-sync` | Optional. Pulls Granola meetings into `research/` and runs `/synthesize` (needs the Granola MCP). |

## Agents

| Agent | Stands in for |
| --- | --- |
| `product-coach` | A senior PM peer who reviews your doc (Cagan, Hoffman, Ries) |
| `discovery-researcher` | A research IC who synthesizes many transcripts into one opportunity |
| `chief-of-staff` (see `chief-of-staff/AGENT.md`) | The person who makes sure meeting intel turns into owned action |

Add more only when you feel the gap: a data analyst (with your analytics MCP), a prototype engineer, a GTM writer, a coach that reviews *you*.

## Authority: the most important part

`CLAUDE.md` has an **Authority** section with three lists: what agents do alone, what they flag to you, and what only you do. Edit it before you trust anything else. Clear boundaries are what make delegation safe.

## Growing it

- Week 1: `/setup` and `/synthesize` on every meeting. Nothing else.
- Week 2: add `/discover` and `/brief` for one real problem.
- Week 3+: add the agent you miss most. Write down one lesson a week in `lessons-learned/`.

Start small. One loop that works beats ten that don't.

## Privacy

This repo will hold customer conversations. Keep your copy **private**, and never commit secrets (see `.gitignore`). The example content here is fictional.
