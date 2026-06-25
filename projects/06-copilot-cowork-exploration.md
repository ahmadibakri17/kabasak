# Copilot Cowork — capability exploration for the team

| Status | Owner | Last updated |
|---|---|---|
| build | Ahmad | 2026-06-25 |

## Problem

Cowork was switched on in the team's M365 Copilot. It's an agentic layer that can *act* across
M365, not just draft — so the team needs a grounded view of what it actually does, where the hard
limits are, and which use cases are worth pursuing, before anyone leans on it. Unstructured
experimentation on a tool that runs under your own identity and bills by usage is how you get a
surprise invoice or a residency problem.

## Current state

- Cowork is **live** for Ahmad / the team; he wants to start hands-on testing.
- No agreed use cases, no guardrails, no view of cost or residency posture yet.

## Target outcome

A reusable exploration kit: a grounded capability/constraints map, a prioritized Controlling
use-case catalog (recurring toil + management simplification, **never** finance-number execution),
and a hands-on test protocol with starter prompt cards Ahmad runs at work on low-sensitivity data —
then feeds results back here. The team ends knowing what Cowork is good for, what it's barred from,
and which 2–3 use cases to take forward.

## Scope boundary (decided)

Cowork is for **coordination, gathering, summarizing, drafting, routing, chasing** — not for
originating, calculating, or transforming financial numbers. That stays in formulas, flows, and
Python, validated. This is non-negotiable and frames the whole catalog.

## Key findings (from research, 2026-06-25 — verify against the tenant)

- **Agentic model:** intent → plan → runs in background → **approval checkpoints** before actions.
  Grounds in Outlook/Teams/Excel/files via "Work IQ".
- 🚩 **Residency gate (#1 open question):** Cowork runs on **Anthropic models, currently *outside*
  the EU Data Boundary**; residency enforcement (where offered) adds ~10% credit cost. Must be
  confirmed with tenant admin/security before any real data.
- **Acts as the user** (actions attributed to Ahmad); **OneDrive/SharePoint files only** (no local),
  no encrypted files, no deletion, 200 MB attachment cap; custom skills aren't Microsoft-validated.
- **Usage-billed** (Copilot Credits ≈ $1–7/task) on top of the Copilot licence; tenants without
  usage billing configured **lose access after 1 Jul 2026**.

## Decisions log

| Date | Decision | Why |
|---|---|---|
| 2026-06-25 | Explore Cowork as a coordination/admin assistant, not a finance-task executor | Sidesteps the deterministic-first/SOX risk; targets the highest-relief, lowest-risk work |
| 2026-06-25 | Full exploration kit + action-oriented (Cowork is live) | User wants to test hands-on now |
| 2026-06-25 | Residency confirmation is a hard pre-flight gate before real data | Anthropic models reported outside EU Data Boundary; charter requires EU residency |

## Open questions

- [ ] **Residency:** does the tenant enforce EU data residency for Cowork, given it runs on
  Anthropic models? (Admin/security to confirm — blocks real-data use until answered.)
- [ ] Is usage-based billing configured (required to keep Cowork past 1 Jul 2026)? What's the
  monthly credit budget / cap?
- [ ] What has the admin enabled — can Cowork post to Teams and send mail on Ahmad's behalf? Which
  SharePoint sites are in reach?
- [ ] Which two use cases does the team feel most pain on, to pilot first?

## Options considered

Captured in `deliverables/06-copilot-cowork-exploration/cowork-use-case-catalog.md` (prioritized).

## Risks & controls

- **Residency** — see gate above; no real data until confirmed. Tests run on low-sensitivity
  synthetic/coordination data only.
- **Attribution** — Cowork acts as Ahmad; never let it send/post unreviewed. Approval gates stay on.
- **Numbers boundary** — no use case originates financial figures; any number is sourced
  deterministically and verified.
- **Cost** — credit consumption watched; budget/cap agreed before heavy use.

## Compliance review

| Date | Verdict | Conditions |
|---|---|---|
| 2026-06-25 | APPROVED WITH CONDITIONS (exploration kit) | (1) Residency confirmed before any real data; (2) tests on low-sensitivity data only; (3) approval gate on every send/post; (4) no finance-number origination; (5) credit budget agreed. See recipe's guardrails section. |

## Deliverables & transfer log

| Artifact | Location | Status |
|---|---|---|
| Capability & constraints map | `deliverables/06-copilot-cowork-exploration/cowork-capability-map.md` | built here |
| Use-case catalog | `deliverables/06-copilot-cowork-exploration/cowork-use-case-catalog.md` | built here |
| Exploration test protocol | `deliverables/06-copilot-cowork-exploration/recipe-cowork-exploration.md` | built here |
| Prompt card — thread summarizer (L1) | `deliverables/06-copilot-cowork-exploration/prompt-thread-summarizer.md` | draft |
| Prompt card — meeting→actions (L2) | `deliverables/06-copilot-cowork-exploration/prompt-meeting-to-actions.md` | draft |
| Prompt card — manager's Monday brief (L3) | `deliverables/06-copilot-cowork-exploration/prompt-manager-monday-brief.md` | draft |

## Next actions

- [ ] Ahmad runs the pre-flight checks (residency, billing, enablement) — recipe step 0.
- [ ] Dry-run not needed at work for L1/L2 cards; carry and test on the mock-equivalent real data
      (a long thread, a meeting transcript) on low-sensitivity content.
- [ ] Report back results → move cards to `verified-at-work`, pick 2 to pilot.
