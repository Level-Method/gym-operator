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

## Step 2 — Location

> Where do you want your gym's files to live? Best is a shared drive — Google Drive, Dropbox, OneDrive — so your team can read them and any AI you use can reach them. A folder on this computer works fine to start.

Create `gym-operations-kb/` there with `gym/`, `gym/operations/`, `work/content/`, `work/members/`, `work/projects/`, `work/reviews/`, `sources/`. Then record the absolute path in both places SKILL.md names: the **Knowledge base location** line in the installed SKILL.md (replace `NOT YET SET` with the path), AND the platform's instructions or memory as backup. One line to the owner: *"Done. That folder is yours — plain files, works with any AI, your team can read it."*

## Step 3 — Collect the inputs

One at a time, each optional:

1. "What's your gym's website address?"
2. "Social accounts you actively post on — links are perfect."
3. "Used ChatGPT a while? Export your history (Settings → Data controls → Export) and I'll mine it."
4. "What software runs your gym — and can you export attendance or membership numbers, names stripped?"

Everything lands in `sources/`, untouched.

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
- `checklist.md` — seeded with the standard Part 2 questions (below) plus anything skipped from Part 1, each with the page it fills and one line on why it matters.
- `index.md` — everything listed, including pages not yet written.
- `log.md` — first entry: knowledge base created, date, built from what.

Then, briefly:

> Set up. index.md shows everything I know; checklist.md is what I still don't — say "continue setup" anytime and we'll knock one or two out.

If you can't write files at their location, give complete file contents and exact paths. Never claim a save that didn't happen.

## Step 7 — Prove it with one real job

> Now let's make it earn its keep. What should we run first?

Offer choices from what THEY said — "you mentioned the fall challenge; want me to prep the promo plan?" Fall back to at most three: weekly review, meeting notes → decisions, lead follow-up prep.

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
- You asked the owner to compose what you could have drafted for confirmation
- Skipping felt like failing, or the checklist felt like homework
- You presented more than one question at a time
- You wrote gym information anywhere inside the skill
- You claimed a save that didn't happen
