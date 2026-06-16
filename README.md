# kabasak — Finance Automation Consulting Workspace

Personal AI consulting team for finance automation in EMEA Controlling (TD SYNNEX, Barcelona):
month-end close, account reconciliations, master data, Special Pricing Conditions, and audit
reporting across 80+ entities.

> **⚠️ Personal device, zero real company data — synthetic/mock samples only, in files and in chat.**

## The operating model

This repo runs on a **personal device** and is **not reachable from work**. The team designs HERE
against mock data; Ahmad executes AT WORK with approved tools, assisted by his work Copilot
(M365 Copilot chat, Copilot in Excel, Copilot Studio). Everything produced here is
**transfer-ready**: one-screen prompt cards, chunked build recipes, and spec-first code that work
Cursor/Copilot regenerates and acceptance tests verify. Results feed back here and the project
briefs keep the memory.

```
design HERE  →  transfer (manual)  →  execute AT WORK  →  feed back  →  iterate
```

## How it works

- **`CLAUDE.md`** — the team charter, loaded into every session: context, the two-environment
  model, approved work toolbox, design principles, deliverable standards.
- **`.claude/agents/`** — the six specialists: `architect`, `power-platform-engineer`,
  `copilot-prompt-engineer`, `python-data-engineer`, `compliance-reviewer` (veto power),
  `strategy-consultant`.
- **`.claude/commands/`** — working modes: `/brainstorm`, `/plan`, `/build`, `/review`.
- **`projects/`** — one brief per project plus `BACKLOG.md`; the team's memory between sessions.
- **`deliverables/`** — transfer-ready outputs per project: recipes, specs, prompt cards,
  reference code.
- **`prompts/`** — general-purpose prompt cards for the work Copilot.
- **`mock-data/`** — synthetic test inputs and generators.
- **`local/`** — git-ignored scratch; never committed.

## Quick start

- **New idea?** `/brainstorm spc intake triage` — or just talk. Keepers go to `projects/BACKLOG.md`.
- **Getting serious?** `/plan <idea>` runs discovery → options → recommendation → execution plan
  (milestones tagged [HERE]/[AT WORK]) → compliance sign-off, and writes the brief.
- **Building?** `/build <thing>` produces the transfer-ready artifact and its at-work checklist.
- **Something already exists at work?** Describe or paste it (anonymized) into `/review <thing>`.
- **Summon anyone directly:** "ask the architect…", "have the compliance reviewer look at this…".
