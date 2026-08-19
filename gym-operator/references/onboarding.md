# Onboarding — setting up the Gym Operations Knowledge Base

By the end, the owner has a knowledge base at a location they chose, with real content in it, has seen it do one real piece of work — and has answered as few questions as possible.

**Read `knowledge-base-structure.md` and `operator-rules.md` before starting.**

## The friction rule

**Confirming beats composing.** Never ask the owner to write from scratch what the sources can answer. Draft it, show it, and let them say "yes," "fix this," or "add this." One confirmation pass replaces eight questions.

**Everything skippable gets skipped gracefully.** Only three things truly require the owner (below). Everything else can be answered now, or skipped to `checklist.md` with a safe default in place. Never make skipping feel like failing.

One question at a time, always. Never a form, never a lecture about the system.

## The shape: two parts

**Part 1 — the basics (today, ~10 minutes).** Location → sources → one confirmation pass → three questions → build the wiki → one real job. Enough to get started and get value.

**Part 2 — the advanced pass (anytime, optional).** The deeper questions that make it better, seeded into `checklist.md` at setup. The owner comes back to them whenever they want, a couple at a time. Getting started never depends on them.

## Step 1 — Welcome

Two sentences, your own words:

> I'm going to set up your gym's knowledge base — the thing that makes me actually know your gym instead of giving generic advice. Most of it I can figure out myself; you'll only need to answer a handful of things.

## Step 2 — Location (Google Drive by default)

**Google Drive is the recommendation, and the owner shouldn't have to decide anything to get it.** Their coaches can open it, it backs itself up, and with Google Drive for Desktop it behaves like an ordinary folder — so Obsidian, this skill, and any other AI read it with no special setup.

Two rules for this whole step: **look before you ask**, and **never make the owner type, paste, or explain a file path.** "Where do you want your files?" is not a question a gym owner can answer well. Find it yourself, do it, and tell them it's done.

### A — Google Drive is already on the machine

Look for it:

- **macOS:** `ls ~/Library/CloudStorage/` → `GoogleDrive-<email>/My Drive/` (older installs: `~/Google Drive/`)
- **Windows:** `G:\My Drive`, or `%USERPROFILE%\Google Drive`

Found it? Create the knowledge base in `My Drive` and report it as **done** — this is a statement, not a question:

> Your gym's files are set up in **Google Drive → My Drive → gym-operations-kb**. They're backed up, your coaches can open them, and any AI you use can read them. (Want them somewhere else? Say so and I'll move them — it takes one second.)

If two Google accounts are signed in, name them and ask which one is the gym's. That is the only question this step may ask when Drive is present.

### B — Google Drive is not on the machine

Recommend it with the exact steps. Never send them off to research it, and never let setup stall on it:

> I'd put these in Google Drive so your coaches can read them and they're backed up automatically. Three minutes:
>
> 1. Download Google Drive for Desktop: https://www.google.com/drive/download/
> 2. Open it and sign in with the Google account you use for the gym
> 3. Say "done" and I'll do the rest
>
> Or if you'd rather not bother right now, say **"just use my computer"** — I'll set it up here in ten seconds, and we can move it into Drive whenever you want. Nothing is lost either way.

If they install it, re-run the detection in A. If they opt out, use `~/Documents/gym-operations-kb/` and add a checklist item: *"Move the knowledge base into Google Drive — it's how your coaches get access."* Never repeat the Drive pitch after they've declined once.

### C — They want something else

Dropbox, OneDrive, iCloud, a specific folder: find it the same way (`~/Dropbox`, `~/OneDrive*`, `~/Library/Mobile Documents/`). If you genuinely can't locate it, ask them to open the folder and drag it into the chat — not to type its path.

### Then, always

Create `gym-operations-kb/` with `assets/`, `gym/`, `gym/operations/`, `work/content/`, `work/members/`, `work/projects/`, `work/reviews/`, `sources/`. Record the absolute path in both places SKILL.md names: the **Knowledge base location** line in the installed SKILL.md (replace `NOT YET SET` with the path), AND the platform's instructions or memory as backup.

### You've gone wrong if

- You asked "where do you want your files?" as an open question
- The owner had to type, paste, or understand a file path
- Setup stalled because they didn't want to install something
- You pitched Google Drive twice

## Step 3 — Collect the inputs

One at a time, each optional:

1. "What's your gym's website address?"
2. "Social accounts you actively post on — links are perfect."
3. "Used ChatGPT a while? Export your history (Settings → Data controls → Export) and I'll mine it."
4. "What software runs your gym — and can you export attendance or membership numbers, names stripped?"
5. "Where do your logo, gym photos, and templates live — a shared drive, a folder somewhere? Link me to it, or drop files in; either works. I'll assume anything you give me is cleared for marketing use — just tell me if someone's off-limits."

Documents and exports land in `sources/`, untouched. Asset locations get mapped in `assets/assets.md` (files the owner hands over directly go in `assets/`).

## Step 4 — Draft everything the sources can answer

Read the sources and **draft the pages** — identity, voice, offers, USP, members, content rhythm, current events — marking each `source:` honestly and anything inferred as `needs-confirming`.

Then present ONE compact recap, not page by page:

> Here's what I've got from your website and Instagram: you're a [X] gym in [Y] for [Z]. You sell [offers]. You sound [voice, one line] — and you'd never say [example]. You post [cadence] and you're running [event] right now. **What's wrong or missing in that?**

End the recap with exactly **one non-obvious observation** from the sources — "One thing I noticed: your website never mentions pricing, but your Instagram answers pricing questions in comments every week." One, not three. Labeled as an observation, never as advice.

Fold their reply in. Only re-present what they corrected.

With no sources at all, skip to Step 5 and ask identity there as a fourth question.

## Step 5 — The questions only they can answer

Three, one at a time:

1. **Goal** — "What are you trying to make happen right now, and by when?" *(e.g. grow to 200 members by December, fill the fall foundations cohort, take a real vacation without the gym stalling)*
2. **Hand-off work** — "What work keeps coming back every week or month — the stuff you'd hand off if you could?" *(e.g. social media posts, promoting your recurring programs, member recognitions — level-up promotions, milestones, birthdays — lead follow-up, weekly numbers, checking in on members who've gone quiet)*
3. **Approvals** — "Anything your team can approve without you?" *(e.g. discounts, refunds, schedule changes, posting to social)* "Until you tell me otherwise I'll assume everything comes back to you." *(This one they can wave off — the default is safe.)*

Then one open door, once:

> There's more I could ask — your values, who your members really are, your constraints — but none of it blocks us. Want to knock any out now, or should I put them on a checklist you can come back to anytime?

Whatever they don't answer goes to the checklist. Safe defaults apply meanwhile: everything returns to the owner for approval; voice mirrors their website and how they write to you; assume their time is scarce.

## Step 6 — Build the wiki + the checklist

Write to THEIR knowledge base:

- Every `gym/` page there's real material for — drafted pages corrected per Step 4, `gym/goals.md` and `gym/rhythm.md` from Step 5.
- A `work/projects/<name>/` folder for each live event named, with a one-paragraph brief.
- `assets/assets.md` — the asset map, from whatever input 5 produced. If assets were skipped, a stub plus a checklist item ("Where do your logo and photos live? Fills assets/assets.md — needed before I can pair photos with posts").
- `checklist.md` — seeded with the standard Part 2 questions (below) plus anything skipped from Part 1, each with the page it fills and one line on why it matters.
- `index.md` — everything listed, including pages not yet written.
- `log.md` — first entry: knowledge base created, date, built from what.

Then, briefly:

> Set up. index.md shows everything I know; checklist.md is what I still don't — say "continue setup" anytime and we'll knock one or two out.

If you can't write files at their location, give complete file contents and exact paths. Never claim a save that didn't happen.

## Step 7 — Prove it with one real job

> Now let's make it earn its keep. What should we run first?

Offer choices from what THEY said — "you mentioned the fall challenge; want me to prep the promo plan?" Fall back to at most three: weekly review, content batch, lead follow-up prep.

No data on hand is never a blocker — every job has a minimum viable input. For the review it's "talk your week at me for sixty seconds."

Run it properly against the fresh knowledge base. Then exactly three questions: **What was useful? What was wrong or generic? What was missing?** Fix it, log the correction, file the output in the right `work/` folder.

## Step 8 — One next thing

One. Not a roadmap. Usually: "Want me to write that up so it runs the same way every week?" Then stop.

## Part 2 — the advanced pass (anytime)

The standard questions seeded into `checklist.md` at setup, alongside anything skipped from Part 1:

| Question | Deepens |
|---|---|
| "What would you turn down money over?" | `gym/values.md` |
| "Who are your members really — why do they join, why do they leave?" | `gym/members.md` |
| "What's the real constraint — time, money, staff, space?" | `gym/goals.md` |
| "What does each person on the team actually own?" | `gym/team.md` |
| "Why does someone drive past two other gyms to get to you?" | `gym/usp.md` |
| "Talk me through how you onboard a new member" *(and other SOPs, one at a time)* | `gym/operations/` |

How it runs:

- Triggered by the owner — "continue setup", "continue the onboarding", "make it better" — never forced. Work through **two or three at a time**, then stop.
- Opportunistic raises: **at most one** per session, and only when relevant to the work at hand: "this draft would be sharper if I knew what you'd turn down money over — answer now or keep skipping?"
- When answered: write the page, check the item off with the date and where it went, log it.
- Never open a session with the checklist. It's an offer, not a nag.

## You've gone wrong if…

- You asked something the sources had already answered
- You asked the owner where to put their files, or made them type a path
- You asked the owner to compose what you could have drafted for confirmation
- Skipping felt like failing, or the checklist felt like homework
- You presented more than one question at a time
- You wrote gym information anywhere inside the skill
- You claimed a save that didn't happen
