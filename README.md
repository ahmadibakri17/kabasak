# kabasak — Finance Automation Consulting Workspace

Personal AI consulting team for finance automation in EMEA Controlling (TD SYNNEX, Barcelona):
month-end close, account reconciliations, master data, Special Pricing Conditions, and audit
reporting across 80+ entities.

> **⚠️ No confidential company data in this repo. Anonymized samples only.**

## How it works

- **`CLAUDE.md`** — the team charter, loaded into every Claude Code session: context, approved
  tools, design principles, and working rules. The team is always briefed; nothing needs
  re-explaining.
- **`.claude/agents/`** — the five specialists: `architect`, `power-platform-engineer`,
  `python-data-engineer`, `compliance-reviewer` (veto power), `strategy-consultant`.
- **`.claude/commands/`** — working modes: `/brainstorm`, `/plan`, `/build`, `/review`.
- **`projects/`** — one brief per project plus `BACKLOG.md` for new ideas. The briefs are the
  team's memory between sessions.
- **`local/`** — git-ignored scratch space; nothing in it is ever committed.

## Quick start

- **New idea?** `/brainstorm spc intake triage` — or just talk. Keepers go to `projects/BACKLOG.md`.
- **Getting serious?** `/plan <idea>` runs discovery → options → recommendation → execution plan →
  compliance sign-off, and writes the project brief.
- **Building?** `/build <thing>` for step-by-step help. **Have something already?**
  `/review <thing>` for a technical + compliance critique.
- **Summon anyone directly:** "ask the architect…", "have the compliance reviewer look at this…".
