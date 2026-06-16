# Month-end close orchestration

| Status | Owner | Last updated |
|---|---|---|
| discovery | Ahmad | 2026-06-11 |

## Problem

Close tasks across entities are tracked manually; status visibility and hand-offs cost time and
chasing during the most time-pressed week of the month. "Where are we?" is answered by asking
people instead of looking somewhere.

## Current state

- Checklist mechanism today not yet captured (Excel? BlackLine Task Management?).
- Some live flows may already touch close steps (reminders, file moves) — pending
  [01-automation-inventory](01-automation-inventory.md).

## Target outcome

One close checklist with owners, dependencies, and statuses; automated reminders instead of manual
chasing; a status view (Power BI or SharePoint) the manager can check daily during close; evidence
links per task so audit requests stop being archaeology.

## Decisions log

| Date | Decision | Why |
|---|---|---|
| 2026-06-11 | Seeded at workspace setup | Core scope area; named priority |

## Open questions

- [ ] How is the close checklist kept today, and who maintains it?
- [ ] How many tasks and entities are in Ahmad's perimeter, and which tasks block which?
- [ ] Is BlackLine Task Management licensed/used? (If yes, the answer may be adoption, not a build.)
- [ ] What does the manager actually want to see daily during close?
- [ ] Which close tasks generate the most chasing today?

## Options considered

To be filled by `/plan month-end close` after discovery. Expected candidates: adopt/extend
BlackLine Tasks if available (simplest — buy not build), SharePoint list + Power Automate
reminders + Power BI status page, Teams-integrated variant.

## Risks & controls

- Orchestration only — this project tracks and reminds; it never posts journal entries or changes
  financial data.
- Reminder flows need error handling and a run log; a silent reminder failure during close is a
  real operational risk.

## Compliance review

| Date | Verdict | Conditions |
|---|---|---|
| — | not yet reviewed | — |

## Deliverables & transfer log

| Artifact | Location | Status |
|---|---|---|
| — | — | — |

## Next actions

- [ ] Capture the current close checklist (structure only, anonymized).
- [ ] Confirm whether BlackLine Task Management is available before designing anything custom.
- [ ] Run `/plan month-end close orchestration`.
