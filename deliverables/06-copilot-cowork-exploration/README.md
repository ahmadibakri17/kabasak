# Cowork exploration kit

| Status | Version | Updated |
|---|---|---|
| draft | v0.1 | 2026-06-25 |

Everything you need to explore Microsoft **Copilot Cowork** for the Controlling team — safely,
on low-sensitivity data, without touching financial numbers. Built here against mock fixtures;
carry it to work and test. Owning brief: `projects/06-copilot-cowork-exploration.md`.

## What's in here

| File | What it's for | Read when |
|---|---|---|
| [`cowork-capability-map.md`](cowork-capability-map.md) | What Cowork can/can't do, residency reality, cost model — grounded and cited | First — know the tool and its limits |
| [`cowork-use-case-catalog.md`](cowork-use-case-catalog.md) | Prioritized Controlling use cases (toil + management), scored, with the numbers-boundary marked | To pick what's worth pursuing |
| [`recipe-cowork-exploration.md`](recipe-cowork-exploration.md) | Pre-flight checks + a hands-on test ladder + observation/feedback templates | When you're ready to actually test at work |
| [`prompt-thread-summarizer.md`](prompt-thread-summarizer.md) | Starter card — Level 1 (read-only summarize) | First hands-on test |
| [`prompt-meeting-to-actions.md`](prompt-meeting-to-actions.md) | Starter card — Level 2 (draft with approval) | Second test |
| [`prompt-manager-monday-brief.md`](prompt-manager-monday-brief.md) | Starter card — Level 3 (multi-step gather + compile) | Third test |

Mock fixtures to rehearse against live in `mock-data/06-copilot-cowork-exploration/`.

## How to use it

1. Read the **capability map** so you know the edges (especially the residency gate).
2. Skim the **use-case catalog** and note which 2–3 resonate.
3. Run the **recipe**: do the 3 pre-flight checks, then climb the test ladder using the three
   prompt cards, recording what you see.
4. Bring the observation log back here — we move the cards to `verified-at-work` and pick the pilots.

## The one rule

Cowork **coordinates, gathers, drafts, summarizes, routes**. It does **not** originate or calculate
financial numbers — ever. Every number stays sourced from a formula, flow, or Python, and verified.
