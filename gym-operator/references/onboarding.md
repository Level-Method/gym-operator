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
- **No shell access to the machine** (claude.ai / Cowork): you can't probe — ask the owner to point you at their Google Drive folder, or grant/drag it into the workspace. One ask, then proceed as if found.

Found it? Create the knowledge base in `My Drive` and report it as **done** — this is a statement, not a question:

> Your gym's files are set up in **Google Drive → My Drive → Gym Operations**. They're backed up, your coaches can open them, and any AI you use can read them. (Want them somewhere else? Say so and I'll move them — it takes one second.)

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

If they install it, re-run the detection in A. If they opt out, use `~/Documents/Gym Operations/` and add a checklist item: *"Move the knowledge base into Google Drive — it's how your coaches get access."* Never repeat the Drive pitch after they've declined once.

### C — They want something else

Dropbox, OneDrive, iCloud, a specific folder: find it the same way (`~/Dropbox`, `~/OneDrive*`, `~/Library/Mobile Documents/`). If you genuinely can't locate it, ask them to open the folder and drag it into the chat — not to type its path.

### Then, always

Create `Gym Operations/` with `assets/`, `gym/`, `gym/operations/`, `work/content/`, `work/members/`, `work/projects/`, `work/reviews/`, `sources/`.

Then record the absolute path in both places SKILL.md names:

1. **`kb-location.md`, in the installed skill folder** — create it and put the absolute path in it, one line, nothing else. It isn't part of the download, so future updates copy over the skill without touching it.
2. **The platform's instructions or memory** — CLAUDE.md, AGENTS.md, or persistent memory — as the backup. If the skill folder can't be written (claude.ai / Cowork, where skills are uploaded through the UI), memory alone is the record — make sure it's actually persisted, not merely mentioned in chat.

Never write the path into `SKILL.md` itself. An update overwrites that file, and the owner silently loses track of their knowledge base.

### Telling them where it went

Say it the way a person would, and **open the folder for them** — `open <path>` on macOS, `explorer <path>` on Windows. A path with a `~` in it is notation, not a location; most owners have never seen one.

> Your files are in your **Documents** folder, in **Gym Operations**. I've just opened it for you.

Never: *"created at `~/Documents/Gym Operations/`."* That sentence is why an owner later can't find their own knowledge base.

### You've gone wrong if

- You asked "where do you want your files?" as an open question
- The owner had to type, paste, or understand a file path
- Setup stalled because they didn't want to install something
- You pitched Google Drive twice
- You reported the location as a path instead of a place, or didn't open it for them

## Step 3 — Ask for the website. That's all.

**One question, not five.**

> What's your gym's website?

Then go read it — and read what it links to. A gym's Instagram and Facebook are almost always linked from its own site, so **find them yourself instead of asking**. Follow them and read the recent posts.

That one answer usually gives you identity, offers, voice, schedule, location, and whatever they're promoting right now — enough to draft the entire first pass.

**No website?**

> No problem — what's your gym's Instagram or Facebook?

Neither of those either? Say so plainly, move to Step 5, and ask identity there as a fourth question.

### The other inputs come later, never upfront

ChatGPT exports, gym-software reports, and photo libraries all make the operator better, and **none of them belong in the first ten minutes**. Nobody should be asked to go export data before they've seen the thing work once.

Seed them into `checklist.md` at Step 6 in plain language, then raise **at most one**, later, and only when a job would visibly have been better with it:

| Checklist item | Raise it when |
|---|---|
| "Where do your logo and photos live? A link to the folder is plenty." | The first content batch has a post with no image to pair |
| "Can your gym software export attendance, with names stripped?" | The first time they ask who's gone quiet |
| "Used ChatGPT for gym stuff? Its history exports, and I'll mine it." | Only if they mention using it |

Never explain how to run an export unprompted. When they ask, give the exact clicks and nothing else.

### If they hand you something anyway

Documents and exports land in `sources/`, untouched. Photo locations get mapped in `assets/assets.md`; files handed over directly go in `assets/`. Use is assumed per the Assets rules — say it once, plainly: *"I'll treat anything you give me as cleared for marketing; just tell me if someone's off-limits."*

## Step 4 — Draft everything the sources can answer

Read the sources and **draft the pages** — identity, voice, offers, USP, members, content rhythm, current events — marking each `source:` honestly and anything inferred as `needs-confirming`.

Then present ONE compact recap, not page by page:

> Here's what I've got from your website and Instagram: you're a [X] gym in [Y] for [Z]. You sell [offers]. You sound [voice, one line] — and you'd never say [example]. You post [cadence] and you're running [event] right now. **What's wrong or missing in that?**

End the recap with exactly **one non-obvious observation** from the sources — "One thing I noticed: your website never mentions pricing, but your Instagram answers pricing questions in comments every week." One, not three. Labeled as an observation, never as advice.

Fold their reply in. Only re-present what they corrected.

With no sources at all, skip to Step 5 and ask identity there as a fourth question.

### If what you read isn't a gym

Owners paste the wrong thing: a franchise's corporate site, a software or supplier company, a personal-brand coaching page, a typo. **Say so before you write anything.** Never reshape a non-gym into a gym to keep the script moving — every page you wrote would be invented, and Step 6 would file the invention as fact.

> That's [what it actually is] rather than a gym itself. Want me to build this around [business], or point me at your gym's site instead?

Write no `gym/` pages until that's settled. If they do want the non-gym business, the knowledge base still works — but say up front which jobs won't apply (anything built on members, classes, or level-ups) instead of letting them find out three weeks in.

### When the socials won't open

Facebook pages are usually login-walled and return nothing. Instagram will often give you the bio and the gist of recent posts, but not full captions. **Don't claim to have read what you couldn't**, and don't let it quietly thin out `gym/voice.md` — voice is the page that makes every draft sound like them.

Build voice from the website copy, mark it `confidence: medium`, and make one small ask at the end of the recap — a paste, never an export:

> One thing that'd sharpen this fast: paste me your last two or three posts. Your website shows me how you write when you're selling; your posts show me how you actually sound.

## Step 5 — What only they can answer

**Only the first of these is genuinely a question.** The friction rule still applies here: anything the sources already answered gets confirmed, not asked.

1. **Goal — ask it cold.** No website tells you what the owner is chasing right now.

   > What are you trying to make happen right now, and by when?

   *(e.g. grow to 200 members by December, fill the fall cohort, take a real vacation without the gym stalling.)* If the goal arrives without a date, ask for the date — the scoreboard in every review and every welcome-back brief is measured against it.

2. **Recurring work — draft it, don't ask it.** You have read their site and their feed by now, so you already know most of what comes back every week. Hand them a list to correct instead of a blank page:

   > From your site and your feed, here's what looks like it comes back around: [posting most days] · [the monthly community event] · [Saturday events and competitions] · [following up on trial sign-ups]. What did I miss — and which of those would you hand off tomorrow if you could?

   The second half is the only part they alone know. Asking the whole thing cold makes them compose a list you could have written.

3. **Approvals — offer it, let them wave it off.**

   > Anything your team can approve without you — discounts, refunds, schedule changes, posting? Until you tell me otherwise, I'll assume it all comes back to you.

   The default is safe, so a shrug is a complete answer. Never ask twice.

Then one open door, once:

> There's more I could ask — your values, who your members really are, your constraints — but none of it blocks us. Want to knock any out now, or should I put them on a checklist you can come back to anytime?

Whatever they don't answer goes to the checklist. Safe defaults apply meanwhile: everything returns to the owner for approval; voice mirrors their website and how they write to you; assume their time is scarce.

## Step 6 — Build the wiki + the checklist

Write to THEIR knowledge base:

- Every `gym/` page there's real material for — drafted pages corrected per Step 4, `gym/goals.md` and `gym/rhythm.md` from Step 5.
- A `work/projects/<name>/` folder for each live event named, with a one-paragraph brief named `<name>-brief.md` — filenames must stand alone in a graph view, so never a generic `brief.md`.
- `assets/assets.md` — a stub, plus the checklist item for where their logo and photos live ("Fills assets/assets.md — needed before I can pair photos with posts"). If they volunteered locations unprompted, map those instead.
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
