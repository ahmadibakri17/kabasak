# Prompt library — for the work Copilot

General-purpose prompt cards for Ahmad's work Copilot. Project-specific cards live with their
project in `deliverables/<NN-slug>/`. Owner: `copilot-prompt-engineer`.

## Conventions

- **Naming by surface:** `chat-*.md` (M365 Copilot chat), `excel-*.md` (Copilot in Excel),
  `studio-*.md` (Copilot Studio instructions/blueprints).
- **One screen max.** Cards are typed at work from a second screen — once — then saved there
  (saved prompts in Copilot, instructions in Studio). `{placeholders}` mark what changes per use.
- **Every card has a "Verify before trusting" section** — the deterministic check that catches a
  bad output. A card without a verification step is not done.
- **Status lifecycle:** `draft → transferred → verified-at-work`, with version + date in the
  header. At-work results (worked / needs tweak / failed how) go into the card's history.
- **Hard line:** cards never ask Copilot to calculate, estimate, or originate financial numbers —
  summarize, classify, draft, restructure, flag, explain only.

Create new cards from `_template.md`.

## Current cards

| Card | Surface | Status |
|---|---|---|
| [chat-close-status-note](chat-close-status-note.md) | M365 Copilot chat | draft |
| [excel-anomaly-scan](excel-anomaly-scan.md) | Copilot in Excel | draft |
