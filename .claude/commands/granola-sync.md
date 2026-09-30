---
description: Optional. Pull new Granola meetings into research/ and hand off to /synthesize (requires the Granola MCP)
---

1. Read `research/.granola-sync-state.json` (create `{"synced": []}` if missing).
2. List Granola meetings since the last sync (or the last 30 days on first run); skip IDs already synced.
3. For each new meeting, get the summary, attendees, and transcript.
4. Save to `research/{topic-subfolder}/YYYY-MM-DD-{slug}.md` in the format in `research/README.md`. Reuse an existing subfolder when the topic fits.
5. Append the meeting ID, date, and path to the state file.
6. Report what was filed, then run `/synthesize` on the new files. Don't stop at filing.
