# AGENTS.md — maintaining this repo

Rules for any AI agent (or human) working on this repository. The README is for gym owners installing the skill; this file is for us.

## Before any work

Pull the latest from `origin/main` first. Others (and other agent sessions) push to this repo; never work from a stale checkout.

## The compiled zip must never go stale

`compiled/gym-operator.zip` is a committed artifact — the download gym owners upload into Claude (Customize → Skills). **Any change to anything under `gym-operator/` requires rebuilding it in the same commit:**

```bash
rm -f compiled/gym-operator.zip && zip -qr compiled/gym-operator.zip gym-operator -x '*.DS_Store' -x '*kb-location.md'
```

Run from the repo root so the zip's root is the `gym-operator/` folder itself (the shape Claude's upload requires). There is deliberately no CI to do this — rebuild locally, every time.

## SKILL.md frontmatter is strict YAML

The `description:` value must parse under a strict YAML parser, not just Claude's lenient one — an unquoted `: ` (colon-space) inside the value breaks `npx skills add` and can break skill-upload validation. After editing frontmatter, verify:

```bash
npx -y skills@latest add ./ --list
```

It must list `gym-operator` with the full description, no parse warnings.

## Keep in sync when the skill changes

- **`gym-operator-skill-explainer.html`** — the diagrams and tables mirror the skill (folder names, onboarding steps, the job list). A skill change that alters any of those needs an explainer pass in the same PR.
- **`README.md`** — install paths, folder names (`Gym Operations`), and job tables must match the skill's current behavior.
- **`gym-operator/CHANGELOG.md`** — entries are for *owner-facing capabilities only* (read aloud to owners after updates). No internal refactors, no repo housekeeping.

## Never commit

- `kb-location.md` (gitignored — it's per-install state written by onboarding)
- Any real gym's data, anywhere. The skill is process only; this rule is the product's "one law."

## Repo practices

- `main` is branch-protected (no force-push, no deletion). Non-trivial changes go through a PR; small fixes may push direct at the owner's discretion.
- This is Level Method's only public repo. Nothing internal — pricing discussions, webinar plans, customer names — belongs in any file here.
- No GitHub Actions or paid CI. Build steps stay local and documented here.
