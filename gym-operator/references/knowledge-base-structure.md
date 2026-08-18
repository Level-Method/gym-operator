# The Gym Operations Knowledge Base — structure

This file is the spec. The knowledge base itself does not exist until onboarding creates it, and it is created at a location the owner chooses — never inside this skill.

## Location principles

- **The owner picks where it lives.** Recommend a shared drive (Google Drive, Dropbox, OneDrive) so their team can read it and any AI platform can reach it. A local folder is fine to start; it can move later.
- **Plain markdown, no lock-in.** Everything is text files. Claude, Codex, or anything else can be pointed at the same folder.
- **Written for humans first.** A coach who has never used AI should be able to open an SOP and follow it. The AI is the second reader.
- Record the location in the project's instructions or memory so every session finds it without asking.

## The layers

```
[owner's chosen location]/gym-operations-kb/
├── index.md          ← catalog of everything, one line each
├── log.md            ← append-only: corrections, decisions, changes
├── checklist.md      ← open questions — skipped during onboarding, answer anytime
├── gym/              ← EVERGREEN — how the gym operates, long-term
│   └── operations/   ← SOPs: one page per process
├── work/             ← CHANGING — outputs of work, by area
│   ├── content/      ← social + website drafts, content calendars
│   ├── members/      ← member-management work: check-ins, at-risk lists, follow-up prep
│   ├── projects/     ← one folder per project or event
│   └── reviews/      ← dated weekly reviews
└── sources/          ← raw material dropped in — read, never edited
```

**`sources/`** — raw material the owner provides: website copy, social posts, a ChatGPT history export, platform exports (names stripped), meeting notes. Read these; never edit them. They are the record.

**`gym/`** — evergreen knowledge you compile and maintain: what the gym is, how it operates, its SOPs. This layer changes rarely and is kept curated. A source might be forty pages; the page you write from it might be nine lines. Compile, don't store.

**`work/`** — the changing layer. Everything the operator produces that lives for a while and then expires or gets archived: content drafts, member-management runs, project and event folders, dated weekly reviews. `gym/` stays evergreen precisely because day-to-day output goes here instead.

**`index.md` + `log.md` + `checklist.md`** — navigation, history, and the open questions. The index tells anyone what exists in thirty seconds. The log is why the operator gets better: read it before every job so a corrected mistake is never repeated. The checklist holds what the owner skipped — each item names the question, the page it fills, and why it matters; unlike the log it is editable, and items get checked off with a date when answered. Raise at most one checklist item per session, only when relevant to the work at hand.

## The pages

| Page | Holds |
|---|---|
| `gym/identity.md` | What the gym is, who it's for, its North Star |
| `gym/values.md` | What they actually stand for — what they'd turn down money over |
| `gym/usp.md` | Why someone picks this gym over the one down the road; who it's NOT for |
| `gym/voice.md` | How they sound, phrases they use, phrases they'd never use, 2–3 real writing samples |
| `gym/offers.md` | What they sell, pricing, what's included, what they won't discount |
| `gym/members.md` | Who they serve — aggregate patterns only, never individuals |
| `gym/team.md` | Real responsibilities, and **who approves what** — discounts, refunds, policy, public posts, spending |
| `gym/goals.md` | Current goal with a date, priorities, constraints, upcoming dates |
| `gym/rhythm.md` | The recurring work: content channels and cadence, event cycles, the weekly and monthly jobs — what comes back, and when |
| `gym/operations/*.md` | One page per SOP — how the gym actually does things. Executable by a human; automatable by AI |

## The working layer — rules

- **Evergreen vs changing:** if it describes how the gym operates, it belongs in `gym/`. If it is an output of work — a draft, a plan, a run of a job — it belongs in `work/`.
- **Date what recurs:** `work/reviews/2026-08-24-weekly-review.md`. A new run never overwrites an old one.
- **One folder per project:** `work/projects/fall-throwdown/` holds everything for that event. When it ends, move the folder to `work/projects/_archive/`.
- **Member work is aggregate:** `work/members/` uses IDs and aggregates, never names with sensitive detail, same privacy rules as everywhere else.
- **Prune-able by design:** `work/` may be cleaned up during the health check; `gym/` and `log.md` are not pruned.
- If a piece of work reveals a stable fact about the gym, the fact is written to `gym/` and logged — the work file is not the system of record.

## Page format

Every `gym/` page starts with:

```markdown
---
updated: YYYY-MM-DD
source: owner interview | website | chatgpt-export | log entry YYYY-MM-DD
confidence: high | medium | needs-confirming
---
```

Mark anything inferred rather than stated as `needs-confirming` and raise it next time it's relevant.

## Linking

Link pages with `[[gym/voice]]` style double brackets. Link generously. A fact needed in two places lives in one page and is linked from the other. Repetition across pages means a page wants to exist.

## Where things belong

| When you learn... | It goes... |
|---|---|
| A stable fact about the gym | The matching `gym/` page, + log entry |
| A correction to your work | `log.md`, + the page it changes if it's a stable fact |
| A decision the owner made | `log.md` |
| How a process works | `gym/operations/<process>.md` |
| Raw material | `sources/` — untouched |
| Content drafted (social, website, email) | `work/content/` |
| A member-management run (check-ins, at-risk, follow-up prep) | `work/members/` |
| Anything for a project or event | `work/projects/<name>/` |
| A weekly review output | `work/reviews/YYYY-MM-DD-weekly-review.md` |
| A new page's existence | `index.md` |
| A new recurring commitment — a channel, an event cycle, a weekly job | `gym/rhythm.md` |
| A new project or event kicking off | `work/projects/<name>/` + noted in `gym/rhythm.md` if it recurs |
| A question the owner skipped or hasn't answered | `checklist.md` — with the page it fills and why it matters |
| A one-time preference | Nowhere — not everything needs saving |

## `log.md` format

Append-only. Never rewrite or delete an entry. Newest at the bottom.

```markdown
## YYYY-MM-DD — short title
**What happened:** one or two lines
**Changed:** [[gym/voice]] — what changed, or "nothing — context only"
**Win** ← optional tag when the owner confirmed a result; the monthly health check counts these
```

## Size discipline

Every page short enough that the owner would actually reread it. Past a screen and a half, split it and link the pieces. The knowledge base should stay small enough to review — it is a working brain, not an archive.
