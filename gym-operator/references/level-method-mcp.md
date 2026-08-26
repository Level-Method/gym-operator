# The Level Method MCP — live gym data

If the gym runs on [Level Method](https://levelmethod.com), the operator can connect directly to their account through the **Level Method MCP** — a secure connector that gives you live access to the roster, levels, the approval queue, promotions, retention dashboards, and Success Sessions. No exports, no stale spreadsheets: the jobs run against what's true right now.

Connector URL: **`https://mcp.levelmethod.com/gym/mcp`**

The knowledge base is still the memory — who the gym is, how it sounds, what it's chasing. The MCP is the eyes and hands into Level Method. They compose: the promotions report tells you *who* leveled up; `gym/voice.md` tells you *how* to celebrate them.

## Who can connect

The sign-in must be a Level Method account with **Admin or owner** role at an active gym — the same login they use for the Level Method gym app. A coach account below Admin can't authorize the connector. If the owner isn't sure of their role, have them try; a failed sign-in almost always means the role, not the password.

**Never ask for their password.** The sign-in happens in their own browser on Level Method's page — you never see or store credentials, and you never type them anywhere.

## Guiding the owner through setup

Offer it when it would help a job, or when they mention Level Method — never as a gate. Two minutes, one sign-in. Give them only the steps for the app they're in:

**Claude desktop app (Cowork) or claude.ai:**

1. Open **Settings → Connectors**, choose **Add custom connector**.
2. Name: `Level Method`. URL: `https://mcp.levelmethod.com/gym/mcp`. Add it.
3. A browser window opens — sign in with their Level Method account and approve access.
4. In a chat, make sure the Level Method connector is enabled in the tools menu. Done — the tools are available in every future session.

(On Team/Enterprise plans an admin may need to allow custom connectors first.)

**Claude Code:**

```bash
claude mcp add --transport http level-method https://mcp.levelmethod.com/gym/mcp
```

Then in a session, run `/mcp` and authenticate when prompted — same browser sign-in.

**ChatGPT desktop app:** Custom connectors live under **Settings → Connectors** (enable **Developer mode** under Advanced settings if the create option is hidden). Create a connector with the URL above, then sign in when prompted. The menu names shift between versions; the constant is: add a connector, paste the URL, sign in through the browser.

**Codex CLI:** add to `~/.codex/config.toml`:

```toml
[mcp_servers.level_method]
url = "https://mcp.levelmethod.com/gym/mcp"
```

(Older Codex versions also need `experimental_use_rmcp_client = true` at the top of the file.)

After connecting, prove it immediately: run one small read — the promotions report or the pending-approvals list — and show the owner something real about their gym. Then note in `log.md` that Level Method is connected.

## What it can do

**Reads** — use freely, in service of the work:

| Tool | What it returns |
|---|---|
| `list_members` | Active members and staff: names, emails, roles, tags, latest level. The starting point — it supplies the `user_id` every member tool needs |
| `get_member_levels` | One member's current level in every MAP category, plus pending levels |
| `get_member_level_history` | One member's level history, newest first |
| `get_levels_summary_grid` | Every member × every category — the whole-gym progress grid |
| `list_pending_level_approvals` | The level-approval queue awaiting a coach's yes/no |
| `get_promotions_report` | Who recently leveled up — rows with an empty `date_printed` still need their certificate printed |
| `get_member_success_history` | One member's Success Session history |
| `get_success_session` | One Success Session in full — notes, outcome, attached plan |
| `get_member_latest_success_plan` | A member's most recent session + Success Plan (purpose, action steps) |
| `success_dashboard_metrics` | Gym-wide Success Plan coverage, session counts, members needing attention |
| `three_factors_snapshot` | The Three Factors retention dashboard — results, relationships, celebrations — with members needing attention |

Programming tools (`list_tracks`, `list_programming_months`, `get_week_programming`) are rolling out and may not appear for every gym yet — use them if they're there, never promise them if they're not.

**Writes** — real actions in the gym's live account:

| Tool | What it does |
|---|---|
| `approve_level` / `reject_level` | Clear the level-approval queue |
| `invite_members` | Email an invite (member, coach, or admin) |
| `suspend_member` / `unsuspend_member` | Deactivate / reactivate a member's access |
| `schedule_success_session` | Book a future Success Session (notifies the coach) |
| `record_success_session` | Log a session that happened |
| `update_success_session` | Edit a session's notes, outcome, or dates |

**Every write follows one rule: propose, then execute only on the owner's explicit yes — one action at a time.** Say exactly what will happen ("approve Jamie's Orange in Squat?"), get the yes, then act. Never batch a blanket approval across members, and never treat a job request ("clear the queue") as pre-approval for each item in it. The server enforces this too — destructive writes return a preview and do nothing without an explicit confirmation — but the owner's yes comes first, always.

This is the one carve-out from the hard line against changing live systems, and it exists because Level Method is the owner's own account, the owner confirms each action, and every action is reversible or auditable inside their gym app.

## How it changes the jobs

- **Member recognitions** — pull `get_promotions_report` instead of asking who leveled up; flag unprinted certificates.
- **Quiet members** — start from `three_factors_snapshot`'s members-needing-attention, not a guess.
- **Weekly review** — fold in `success_dashboard_metrics`, the approval-queue depth, and the week's promotions.
- **Success Sessions** — pull `get_member_latest_success_plan` up live while the owner runs one; offer to record it after.
- **Approval queue** — list it, then walk it one confirmed decision at a time.

Each job's minimum-viable-input rule still holds: no connection is never a blocker, it's just more asking.

## Live data and the knowledge base

- Live data is for the work, not for copying. Don't mirror the roster or any member's record into the knowledge base — the privacy rules there don't move: aggregate patterns and IDs, never individuals with sensitive detail.
- Log every write action in `log.md` (what, who asked, when), same as any decision.
- If live data contradicts a `gym/` page (member count, offer names), trust the live data and flag the page for the health check.

## When it breaks

- **Sign-in loop or 401s** — the token expired or was revoked: reconnect (re-authenticate the connector; in Claude Code, `/mcp` → reconnect).
- **Sign-in refused** — the account is likely below Admin at the gym, or the gym isn't active. The owner fixes roles inside Level Method, not here.
- **Tools missing from the list** — the connector isn't enabled for the chat, or (for programming tools) not rolled out yet.
- Never work around a failed connection by asking the owner to paste passwords or export data they didn't offer — fall back to the job's minimum viable input and move on.
