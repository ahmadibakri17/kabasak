# Automation inventory & hardening

| Status | Owner | Last updated |
|---|---|---|
| discovery | Ahmad | 2026-06-11 |

## Problem

Production automations (Power Automate flows, scripts) already run, but there is no single
register of what exists, what each one does, who owns it, or whether each would survive an audit
question. Every new design risks duplicating or breaking something live, and undocumented
automations touching financial processes are a latent SOX finding.

## Current state

- Live Power Automate flows and scripts confirmed in production (2026-06-11), inventory not yet
  consolidated anywhere.
- No central register in this repo or (as far as known) elsewhere.

## Target outcome

A living register — in this repo or as a SharePoint list — with one row per automation: name,
purpose, trigger, inputs/outputs, owner, last change, logging status, and control gaps. Plus a
prioritized hardening list (logging, error alerts, documentation, segregation of duties). This is
the foundation every other brief builds on, and it is itself a control improvement worth telling
internal audit about.

## Decisions log

| Date | Decision | Why |
|---|---|---|
| 2026-06-11 | Seeded as the foundation project at workspace setup | Brownfield landscape must be mapped before any new design; avoids duplication/breakage and strengthens SOX posture |

## Open questions

- [ ] Roughly how many flows and scripts are live? Which areas (close, recs, SPC, reporting)?
- [ ] Where do they live — personal "My flows" or solution/environment-managed?
- [ ] Are any owned by other people or shared accounts?
- [ ] Which ones touch financial data directly (vs notifications/reminders)?
- [ ] Have any failed silently before? How was it noticed?
- [ ] What documentation exists today, if any?

## Options considered

To be filled by `/plan automation inventory` after discovery.

## Risks & controls

- Risk while inventorying: none — read-only exercise.
- Watch for: real entity/system names in the register if kept in this repo → keep the detailed
  register in SharePoint, an anonymized summary here.

## Compliance review

| Date | Verdict | Conditions |
|---|---|---|
| — | not yet reviewed | — |

## Next actions

- [ ] Export the list of flows from make.powerautomate.com (My flows + Shared with me) — names and
  descriptions only.
- [ ] List scripts (Office Scripts library + anything in Python) the same way.
- [ ] Bring the anonymized list to a `/build automation inventory` session to structure the register.
