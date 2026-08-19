# Gym Operator

An AI operator for gym owners, by [Level Method](https://levelmethod.com).

Point your AI assistant at this repo and it becomes an operator that actually knows **your** gym — your voice, your offers, your goals, your people — instead of giving generic fitness-business advice. It sets up a **Gym Operations Knowledge Base** (plain markdown files, stored wherever you choose, owned by you forever) and then does real recurring work grounded in it.

## Why

You already pay for AI. Ask it a blank-chat question and you get decent generic advice — the same advice every other gym gets. The real divide isn't between owners who use AI and owners who don't. It's between asking for occasional help and building something around it that persists.

> AI supplies the intelligence.
> Context makes it relevant.
> A process makes it repeatable.

This skill supplies the context and the process:

- **Your gym, on paper.** One folder holds who you are, how you sound, what you sell, what you're chasing this quarter, and how your gym actually runs — plus your logo, photos, and templates (or links to wherever those already live), so drafted posts come paired with the right image. Every answer is grounded in that — and every output quietly shows which of your pages it drew from.
- **It compounds.** In a normal chat, your corrections die when the conversation ends. Here, every correction and decision is written into the knowledge base, so next week's work starts where last week's left off. Within a couple of sessions the drafts stop sounding like AI and start sounding like you.
- **Real work, on a rhythm.** Weekly reviews scored against your goal, content batches in your voice, member recognitions, lead follow-up prep, quiet-member check-ins, event promos — each a written procedure, not a lucky prompt.
- **You stay the owner.** It drafts, preps, and recommends behind the counter. It never posts, sends, or talks to a member — people come to a gym for people.
- **No lock-in, ever.** Plain markdown in a folder you own. Point Claude at it today, something else next year — the knowledge base outlives any platform, and this skill.

## The fastest way to install

Copy this into your AI assistant (Claude Code, Claude Desktop, Codex, or any agent that can read files and run commands):

> Install the Gym Operator skill from https://github.com/Level-Method/gym-operator — follow the install instructions in the README, then start my onboarding.

That's it. The agent will install the skill and walk you through a ~10 minute setup: it reads your website and socials, drafts what it can, asks you only what it can't figure out, and then runs its first real job for you.

## What it does

Six jobs ship today, each with a written procedure:

| Job | What you get |
|---|---|
| **Weekly review** | What changed, what needs attention, your decisions, three priorities — scored against your current goal, every week |
| **Content batch** | A week of posts in *your* voice, ready for you to post |
| **Member recognitions** | Level-ups, milestones, birthdays — shout-outs and notes drafted so recognition never slips |
| **Lead follow-up prep** | This week's inquiries prioritized with drafts attached |
| **Quiet members** | Who's drifting before they cancel, with a personal check-in drafted for each |
| **Event promo** | A dated promo plan plus every draft, worked back from event day |

Plus: a welcome-back brief every session (it knows what week it is and what's coming up), SOP capture ("write up how we onboard members"), a monthly health check, and a wins scoreboard built from your own log.

## The rules it lives by

- **Your data is yours.** Everything about your gym lives in *your* knowledge base — a folder of plain markdown files, set up in your Google Drive by default so your coaches and any AI platform can read it (somewhere else is fine too; you'll be asked nothing you can't answer). The skill contains process only. Delete the skill and your knowledge base still works with any AI, forever.
- **It never touches the outside world.** It drafts, preps, analyzes, and recommends. It never sends, posts, publishes, schedules, purchases, or talks to your members. You stay the owner.
- **It never stores** passwords, payment details, medical/injury info, or member data you don't have permission to share.

## Install instructions (for the AI agent)

If you are an AI agent installing this skill for a gym owner:

1. **Get the files.** No git required — download and extract the repo:

   ```bash
   curl -L https://github.com/Level-Method/gym-operator/archive/refs/heads/main.tar.gz | tar xz
   ```

   (`git clone https://github.com/Level-Method/gym-operator.git` works too, if git is available.)

2. **Copy the `gym-operator/` folder** (the one containing `SKILL.md`) into your platform's skills location:
   - **Claude Code (personal, all projects):** `~/.claude/skills/gym-operator/`
   - **Claude Code (one project):** `<project>/.claude/skills/gym-operator/`
   - **Claude Desktop / claude.ai (no shell access):** the owner uploads the `gym-operator` folder as a skill under **Settings → Capabilities** instead of copying files.
   - **Cursor / Codex / other agents:** wherever your platform loads skills or custom instructions from; if it has no skills system, keep the folder anywhere the owner can point you at and read `SKILL.md` at the start of each session.

   Example for Claude Code:

   ```bash
   cp -R gym-operator-main/gym-operator ~/.claude/skills/gym-operator
   ```

   The downloaded archive can be deleted after copying — the installed folder is the skill.

3. **Read the installed `SKILL.md`** and follow it. For a new owner, that means running the onboarding in `references/onboarding.md` — it creates the knowledge base at a location the owner chooses, then **writes that path into the installed `SKILL.md`** (the "Knowledge base location" line) and into your platform's memory/instructions, so every future session finds it without asking.

4. **Confirm to the owner** what was installed and where, then begin onboarding.

## Updating

Tell your agent:

> Update my Gym Operator skill from https://github.com/Level-Method/gym-operator

The agent should download the latest files the same way as install and copy them over the installed folder. Where your knowledge base lives is recorded in `kb-location.md`, which isn't part of the download — the copy leaves it alone, so there's nothing to restore afterward. (Installed before that file existed? The path is on a "Knowledge base location" line in the old `SKILL.md` — save it first, then write it into `kb-location.md`.)

When copying over an existing install, keep the trailing slashes — without them `cp` nests the new folder *inside* the old install instead of replacing its contents:

```bash
cp -R gym-operator-main/gym-operator/ ~/.claude/skills/gym-operator/
```

Your knowledge base itself is never touched by updates. On the next session, the operator reads `CHANGELOG.md` and tells you what's new in two lines — and offers one new capability tied to your gym.

## Browsing your knowledge base like a wiki

Your knowledge base is plain markdown, so you can read it anywhere — but it's much nicer in [Obsidian](https://obsidian.md), a free app (Mac, Windows, Linux, iPhone, Android) that turns a folder of markdown files into a clickable wiki:

1. Download Obsidian from [obsidian.md](https://obsidian.md/download) and open it.
2. Choose **Open folder as vault** (on the vault picker, or via the vault switcher at the bottom-left) and select your `gym-operations-kb` folder.
3. That's it. Every page renders cleanly, the `[[double-bracket]]` links between pages become clickable, and the graph view shows how your gym's knowledge connects.

Because the vault is just your folder, there's no sync or export step — the operator writes a page, and it's there the next time you look. Your coaches can do the same on their own machines if the knowledge base lives on a shared drive. (If Obsidian prompts about trusting the vault or restricted mode, accepting the safe defaults is fine — the knowledge base uses no plugins.)

## What's in this repo

```
gym-operator/
├── SKILL.md                          ← the operator: the loop, routing, hard lines
├── CHANGELOG.md                      ← what's new, read after every update
└── references/
    ├── onboarding.md                 ← the ~10 minute setup
    ├── knowledge-base-structure.md   ← the spec for YOUR knowledge base
    ├── operator-rules.md             ← how it behaves, always
    ├── maintenance.md                ← ingest + monthly health check
    └── jobs/                         ← the six job procedures
```

No gym data ever lives in this repo — that's the point.

Also here: [gym-operator-skill-explainer.html](gym-operator-skill-explainer.html) — a one-page visual explainer of how the skill and your knowledge base fit together (download it and open it in a browser).

## Questions

Open an issue, or reach out to Level Method.
