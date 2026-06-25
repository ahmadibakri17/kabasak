# Cowork use-case catalog — EMEA Controlling

| Status | Version | Updated |
|---|---|---|
| draft | v0.1 | 2026-06-25 |

Prioritized use cases for Cowork as the team's **coordinator**, not its accountant. Two buckets:
recurring team toil, and lifting manual work off management. Scored 1–5 (5 = best). **Risk** scores
data sensitivity + attribution exposure (5 = lowest risk). Nothing here originates financial
numbers.

**Reading the table:** *Impact* = hours/relief; *Effort* = setup + prompt tuning; *Risk* = how safe
(higher is safer). "Gate" flags use cases that need the residency answer or specific admin
enablement before real-data use.

## Bucket A — recurring team toil

| # | Use case | What Cowork does | Data + sensitivity | Human checkpoint | Verify before trusting | I/E/R | Gate |
|---|---|---|---|---|---|---|---|
| A1 | **Thread / channel summarizer** | Condenses a long email thread or Teams channel to a 5-line "where it stands" + open points | Mail/Teams text — low/med | Read before relying | Spot-check claims vs the thread; no invented commitments | 4/5/4 | residency |
| A2 | **Meeting → actions** | Turns a meeting transcript into assigned, dated action items + draft follow-ups | Transcript — low/med | Approve before any send/schedule | Every action traces to a transcript line; owners exist | 5/4/4 | residency |
| A3 | **Deadline reminder runner** | Drafts timely nudges to owners of recurring close/audit/SPC tasks | Task list + calendar — low | Approve sends | Right owners, right dates vs the list | 4/4/4 | post-on-behalf |
| A4 | **Shared-mailbox triage** | Classifies incoming requests, logs to a SharePoint list, drafts acknowledgments | Shared mailbox — med | Approve logging/replies | Each item categorized correctly; nothing dropped | 4/3/3 | residency + enablement |
| A5 | **"What changed while I was out"** | Catch-up brief after leave from mail + Teams + calendar | Personal M365 — low/med | Read only | Cross-check a few items against source | 3/5/4 | residency |
| A6 | **SOP knowledge concierge** | Answers "how do we do X?" from documented team procedures | SOP docs in SharePoint — low | Read only | Answer matches the SOP; flags when unsure | 4/4/5 | none (low-sensitivity) |

## Bucket B — simplify for management

| # | Use case | What Cowork does | Data + sensitivity | Human checkpoint | Verify before trusting | I/E/R | Gate |
|---|---|---|---|---|---|---|---|
| B1 | **Manager's Monday brief** | One weekly digest: open close tasks, audit deadlines, unanswered requests, team calendar | Several M365 sources — med | Manager reads | Counts/dates trace to source lists; numbers only quoted, never computed | 5/3/4 | residency |
| B2 | **Close-review prep pack** | Compiles status, risks, open items into the manager's talking points before the review | Close tracker + notes — med | Manager reviews | Status reflects the tracker; risks sourced, not invented | 5/3/4 | residency |
| B3 | **Upward-update drafter** | Drafts the manager's recurring status note to their boss/regional controller | Team notes/actuals — med | Manager edits + owns it | Every figure quoted from a sourced report, not generated | 4/4/3 | residency |
| B4 | **Approvals & action chaser** | Tracks what's waiting on the manager and nudges, so nothing stalls | Approvals/inbox — med | Manager approves nudges | Items real and still open; no duplicate chasing | 4/4/4 | post-on-behalf |
| B5 | **Onboarding concierge** | Walks a new joiner through who-owns-what, where things live, what's due | Team docs — low | Read only | Matches current org/SOP docs | 3/4/5 | none |

## The numbers boundary (applies to every row)

Where a use case shows a figure (B1, B2, B3), Cowork is **quoting a number from a source it was
given** — a finished report, a tracker cell — never calculating one. If a task tempts you to ask
Cowork to total, vary, or reconcile, that's the signal to stop and use a formula/flow/Python
instead, then hand Cowork the result to write up.

## Recommended first three (lowest risk × highest relief)

1. **A2 Meeting → actions** — universal pain, instant payoff, easy to verify. *Test card provided.*
2. **A1 Thread/channel summarizer** — the safest possible start (read-only), proves grounding
   quality. *Test card provided.*
3. **B1 Manager's Monday brief** — highest visibility; the management-relief flagship once A1/A2
   build confidence. *Test card provided.*

A6 (SOP concierge) is the best *un-gated* option if the residency answer is delayed — it runs on
low-sensitivity procedure docs and helps the whole team immediately.

## Mapping back to existing projects

- A2/B1/B2 feed **`04-month-end-close`** (status visibility, less chasing).
- A4 feeds **`05-audit-sox-reporting`** (request intake).
- A3 supports **`03-special-pricing-conditions`** (chasing incomplete intake — Cowork chases,
  deterministic logic still validates).
