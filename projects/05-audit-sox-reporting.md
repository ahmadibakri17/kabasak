# Audit & SOX reporting support

| Status | Owner | Last updated |
|---|---|---|
| discovery | Ahmad | 2026-06-11 |

## Problem

Recurring audit and SOX requests — populations, evidence packs, PBC items — require repetitive
data pulls and reformatting every cycle. Each request is handled as if it were new, and turnaround
competes with close work.

## Current state

- Workiva is the reporting backbone; request handling is manual and formats vary by requester.
- Possible overlap with existing scripts/flows — pending
  [01-automation-inventory](01-automation-inventory.md).

## Target outcome

A library of repeatable, logged extract-and-format routines for the recurring requests: same
request next cycle = run the routine, not rebuild it. Evidence packs reproducible on demand with a
run log (what was pulled, when, from where, by whom). Faster turnaround, and the reproducibility
itself is an audit selling point.

## Decisions log

| Date | Decision | Why |
|---|---|---|
| 2026-06-11 | Seeded at workspace setup | Core scope area; named priority |

## Open questions

- [ ] What are the recurring requests per cycle (internal audit, external audit, SOX testing)?
- [ ] Source systems per request — SAP, BlackLine, Workiva, others?
- [ ] Required formats and who defines them?
- [ ] Deadlines/SLAs, and where turnaround hurts most today?
- [ ] What does Workiva already automate here that is simply not being used?

## Options considered

To be filled by `/plan audit reporting` after discovery. Expected candidates: parameterized Power
Query/Office Script templates per request type (simplest), Python extract library with run logging
(strongest evidence trail), Workiva-native features first wherever they exist.

## Risks & controls

- Population completeness is the control that matters: every extract carries row counts and
  control totals against source.
- Extracts contain real data by nature — they live in SharePoint/Workiva, never in this repo;
  only anonymized format examples here.

## Compliance review

| Date | Verdict | Conditions |
|---|---|---|
| — | not yet reviewed | — |

## Next actions

- [ ] Inventory last cycle's requests; rank by frequency × effort.
- [ ] Pick the top one as pilot; collect an anonymized format example.
- [ ] Run `/plan audit and SOX reporting`.
