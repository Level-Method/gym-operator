# Maintenance — ingest and health check

Two procedures that keep the knowledge base alive instead of rotting.

## Ingest — when new raw material arrives

A website update, an export, meeting notes, a season of social posts:

1. File it in `sources/`, untouched.
2. Read it and determine which `gym/` pages it affects — one source may touch several.
3. Update those pages. Compile, don't paste: forty pages of source might change nine lines of knowledge.
4. Note contradictions with existing pages — surface them to the owner rather than silently overwriting. Sometimes the old page is right and the new material is wrong.
5. Log what changed. Update `index.md` if pages were added.

## Health check — monthly, or on contradiction

Run when a month has passed, when a correction reveals wrongness in several places, when a job keeps needing information no page holds, or when something big changed (new coach, new pricing, new location).

Read everything in `gym/`, plus `index.md` and `log.md`. Check seven things:

1. **Contradictions** — two pages disagree. Report both versions.
2. **Expired goals and dates** — `gym/goals.md` says "+12 by Sept 30" and it's November. Flag and ask for the current goal.
3. **Unconfirmed guesses and open questions** — `needs-confirming` pages that never got confirmed, and `checklist.md` items that have sat for months. List them; offer to knock out one or two.
4. **Orphans** — pages nothing links to or reads.
5. **Bloat** — pages past a screen and a half. Propose splits.
6. **Gaps** — information jobs keep needing that no page holds. That's a page that wants to exist.
7. **Stale work/** — finished projects not yet archived, drafts nothing came of. Propose archiving or pruning. (`gym/` and `log.md` are never pruned.)

## Output

Open with **the scoreboard** — the month's log entries tagged **Win**, counted plainly: "This month: 4 weekly reviews, 11 posts drafted, 3 drifting members caught, the fall challenge promo shipped on time." This is the owner's answer to "is this worth it," written from their own log.

Then, short and grouped:

**Needs the owner:** contradictions (both versions) · expired goals · guesses to confirm.
**Fixable on approval:** splits, merges, orphan removals, link repairs.
**Missing:** pages that should exist.

## Never

Fix silently — this reports and proposes; the owner decides. Delete a page without asking. Assume newest is correct.

Log everything that changes.
