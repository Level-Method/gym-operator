# Gym Operator

An AI operator for gym owners, by [Level Method](https://levelmethod.com).

Point your AI assistant at this repo and it becomes an operator that actually knows **your** gym — your voice, your offers, your goals, your people — instead of giving generic fitness-business advice. It sets up a **Gym Operations Knowledge Base** (plain markdown files, stored wherever you choose, owned by you forever) and then does real recurring work grounded in it.

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

- **Your data is yours.** Everything about your gym lives in *your* knowledge base — a folder of plain markdown files at a location you choose (a shared drive is best so your team and any AI platform can read it). The skill contains process only. Delete the skill and your knowledge base still works with any AI, forever.
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

The agent should: note the current "Knowledge base location" line in the installed `SKILL.md`, download the latest files the same way as install, copy them over the installed folder, and **re-set the location line** in the new `SKILL.md`. Your knowledge base itself is never touched by updates. On the next session, the operator reads `CHANGELOG.md` and tells you what's new in two lines — and offers one new capability tied to your gym.

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

## Questions

Open an issue, or reach out to Level Method.
