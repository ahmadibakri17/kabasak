# Account reconciliation automation

| Status | Owner | Last updated |
|---|---|---|
| discovery | Ahmad | 2026-06-11 |

## Problem

Reconciliation preparation and substantiation across 80+ entities is largely manual: gathering SAP
data, tying out balances, and preparing BlackLine-ready support eats recurring hours every close
and carries error risk in the least glamorous part of the work.

## Current state

- BlackLine is the system of record for reconciliations; SAP is the data source.
- Unknown which prep steps are already assisted by existing flows/scripts — pending
  [01-automation-inventory](01-automation-inventory.md).

## Target outcome

A deterministic rec-prep pipeline: source data in → tiered matching (exact → composite → tolerance)
→ exception queue for human review → substantiation pack out. BlackLine remains the system of
record; humans certify. Same engine, config per entity. Hours drop, and every run leaves an audit
trail (control totals, run log, immutable outputs).

## Decisions log

| Date | Decision | Why |
|---|---|---|
| 2026-06-11 | Seeded at workspace setup | Core scope area; named priority |
| 2026-06-11 | Direction: deterministic matching engine, human certifies in BlackLine | Charter principles — no LLM near the numbers; HITL gate |

## Open questions

- [ ] Which rec types consume the most hours — intercompany, bank, GR/IR, accruals, other?
- [ ] What are the data sources and formats (SAP export transactions used, BlackLine import
  templates)?
- [ ] Monthly volumes: how many recs, how many line items in the painful ones?
- [ ] What matching/tolerance rules are applied today, and are they written down anywhere?
- [ ] Who certifies, and what does "good support" look like to the reviewer?

## Options considered

To be filled by `/plan account reconciliations` after discovery. Expected candidates: Power Query
template per rec type (simplest), Python tiered-matching engine (scales best), Office Script +
flow hybrid.

## Risks & controls

- No fuzzy auto-matching into the books — anything below exact/configured-tolerance goes to a human.
- Completeness control: matched + exceptions = input, by count and amount, or the run fails loudly.
- Anonymized fixtures only in this repo.

## Compliance review

| Date | Verdict | Conditions |
|---|---|---|
| — | not yet reviewed | — |

## Deliverables & transfer log

| Artifact | Location | Status |
|---|---|---|
| — | — | — |

## Next actions

- [ ] Pick the single most painful rec type as the pilot candidate.
- [ ] Prepare one anonymized sample dataset (input + expected matches) for fixtures.
- [ ] Run `/plan account reconciliations`.
