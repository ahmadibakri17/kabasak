# Special Pricing Conditions (SPC) workflow

| Status | Owner | Last updated |
|---|---|---|
| discovery | Ahmad | 2026-06-11 |

## Problem

Special Pricing Conditions involve intake, validation, tracking, and reporting across entities —
manual touchpoints, scattered status visibility, and standing audit attention because pricing
conditions affect revenue and margin.

## Current state

- Process details not yet captured in this workspace; some automation may already exist — pending
  [01-automation-inventory](01-automation-inventory.md).

## Target outcome

A structured pipeline: intake via form/list instead of inbox, deterministic validation rules,
status tracking visible to everyone involved, approval trail preserved, and reporting that answers
management and audit questions without manual assembly. SAP stays the system of record for
condition records; humans approve.

## Decisions log

| Date | Decision | Why |
|---|---|---|
| 2026-06-11 | Seeded at workspace setup | Core scope area; named priority |

## Open questions

- [ ] What is the intake channel today — email, Excel files, something else?
- [ ] Monthly volume of SPC requests, and how spiky is it?
- [ ] Which validation rules decide accept/reject/escalate, and are they documented?
- [ ] Who approves, at what thresholds? Where does the approval live today?
- [ ] Where does the result land (SAP condition records?) and who keys it in?
- [ ] What reports do management and audit ask for, and how are they produced now?

## Options considered

To be filled by `/plan special pricing conditions` after discovery. Expected candidates:
SharePoint list + Power Automate approvals (simplest), Power Apps front end on top, Copilot Studio
intake/triage front door (classification only) feeding the same deterministic pipeline.

## Risks & controls

- Validation logic must be deterministic and versioned; an LLM may at most classify/triage an
  incoming request, never decide a condition's values.
- Approval trail must be reconstructible — approvals logged with who/when/what.
- Anonymized examples only in this repo (Customer C-0042, invented discounts).

## Compliance review

| Date | Verdict | Conditions |
|---|---|---|
| — | not yet reviewed | — |

## Deliverables & transfer log

| Artifact | Location | Status |
|---|---|---|
| — | — | — |

## Next actions

- [ ] Walk through the current process end-to-end in a discovery session — actors, hand-offs,
  systems touched.
- [ ] Collect one anonymized example request from intake to SAP entry.
- [ ] Run `/plan special pricing conditions`.
