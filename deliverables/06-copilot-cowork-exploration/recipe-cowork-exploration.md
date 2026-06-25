# Recipe — explore Cowork safely (hands-on)

| Status | Version | Updated |
|---|---|---|
| draft | v0.1 | 2026-06-25 |

A step-by-step way to get hands-on with Cowork without tripping a residency, cost, or attribution
problem. Do the pre-flight once, then climb the ladder. Use **low-sensitivity data only** until the
residency gate is cleared. Pair this with the three prompt cards in this folder.

---

## Step 0 — Pre-flight checks (do these first, once)

Don't put any real content in until these three are answered.

**0a. Residency** — ask your tenant admin / security, in writing:
> "For Copilot Cowork, where is task processing performed, and does it stay within the EU Data
> Boundary? Cowork runs on Anthropic models — are those covered by our EU residency commitments, or
> processed outside the EUDB?"
- ✅ *Checkpoint:* you have a written answer. If "outside EUDB / not covered," **stop at
  low-sensitivity synthetic data** and raise with compliance before any real Controlling data.

**0b. Billing** — confirm usage-based billing (Copilot Credits) is configured and a budget/cap is
set.
- ✅ *Checkpoint:* billing is on (required to keep Cowork past **1 Jul 2026**) and you know the
  monthly cap.

**0c. Enablement** — confirm what Cowork may do for you: read which mailboxes/sites, **post to
Teams**, **send mail on your behalf**.
- ✅ *Checkpoint:* you know which test rungs are even possible (sending/posting needs 0c).

---

## The test ladder

Climb one rung at a time. Each rung: pick safe data, run the card, watch the plan, **approve
nothing you haven't read**, and record what you saw in the log below.

### Level 1 — read-only summarize *(safest; start here)*
- **Card:** `prompt-thread-summarizer.md`
- **Data:** a long but low-sensitivity email thread or Teams channel (a logistics/scheduling thread,
  not a customer or close-numbers thread).
- **Do:** run the prompt, let Cowork summarize. No actions, nothing sent.
- **Watch for:** Did it ground in the *actual* thread or drift/invent? Did it respect the length and
  structure you asked for?
- ✅ *Pass if:* the summary is accurate, sourced, and admits what it doesn't know.

### Level 2 — draft with approval
- **Card:** `prompt-meeting-to-actions.md`
- **Data:** a transcript from a low-sensitivity internal meeting (a team sync, not a sensitive
  review).
- **Do:** let it extract actions and **draft** follow-ups — then stop at the approval gate. Don't
  send (or send one to yourself only).
- **Watch for:** Does every action trace to something actually said? Are owners/dates right? Does it
  pause for approval as expected?
- ✅ *Pass if:* actions are faithful and nothing sends without your click.

### Level 3 — multi-step gather + compile
- **Card:** `prompt-manager-monday-brief.md`
- **Data:** low-sensitivity coordination sources (a task list, a calendar, an open-items list) — no
  real financial figures.
- **Do:** let it run the multi-step plan and produce one brief. Observe the checkpoints.
- **Watch for:** Does it pull from the right sources? Does it *quote* numbers from the source rather
  than computing any? How many credits did the run cost?
- ✅ *Pass if:* the brief is accurate, every figure is quoted-not-calculated, and the cost is
  acceptable.

---

## Observation log (copy one block per run)

```
Run: L_  | Card: _______________ | Date: ______
Data used (low-sensitivity? Y/N): ______
Grounded in real source? (Y / drifted / invented): ______
Approval gate behaved as expected? (Y/N): ______
Output quality (1–5): __   Notes: ______________________
Credits/cost for the run: ______
Verdict: works / needs tweak / failed — how: ______________
```

## Feedback to bring back here

After a session, paste your logs into a `/build` or `/review` chat. We'll:
- tune the cards and move passing ones to `verified-at-work`,
- update the use-case catalog scores with real cost/quality data,
- pick the two use cases to pilot for the team/management.

---

## Guardrails (compliance — non-negotiable during exploration)

1. **Residency gate** — no real Controlling data until 0a is answered acceptably. Synthetic/
   low-sensitivity only before that.
2. **Data sensitivity** — never test on real financial figures, customer/vendor master data, or
   anything traceable to an entity. Coordination/admin content only.
3. **Attribution** — Cowork acts as *you*. Read everything before approving a send/post; treat its
   drafts as yours.
4. **Numbers boundary** — never ask Cowork to total, calculate, vary, or reconcile. It quotes
   sourced numbers; it never makes them.
5. **Cost** — note credits per run; stop if a task type is burning more than it saves.

If a use case graduates from exploration to something recurring or production-like, it comes back
through `/plan` for a full compliance sign-off before it's real.
