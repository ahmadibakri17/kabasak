# Cowork capability & constraints map

| Status | Version | Updated |
|---|---|---|
| draft | v0.1 | 2026-06-25 |

A grounded reference so you explore with eyes open. Sources are public Microsoft docs and launch
coverage as of June 2026 — **treat every residency, cost, and governance line as "confirm against
our tenant," not gospel.** Links at the bottom.

## What Cowork is

Copilot Cowork (generally available 16 Jun 2026) is the **agentic** layer of M365 Copilot. Plain
Copilot drafts and suggests in the moment; Cowork takes a goal and **executes a multi-step task end
to end** — it breaks your request into a plan, works it in the background across your M365 apps
(grounded by "Work IQ" over Outlook, Teams, Excel, files), and **pauses at checkpoints for you to
approve** before anything leaves your hands.

The mental model that keeps you safe: **Cowork is a fast, literal junior who will do the legwork and
show you the result for sign-off — never the person who owns the numbers.**

## How you interact with it

1. You describe the outcome ("summarize this thread", "draft a recap and send to my team", "compile
   a status from these sources").
2. Cowork turns it into a plan and works step by step; you can watch the steps appear.
3. Before any *action* (send, post, create, schedule), it shows you what it intends to do and waits
   for approval.
4. Available at m365.cloud.microsoft, the M365 Copilot desktop app, and mobile.

## What it can do (the useful surface for us)

- **Read & summarize** across mail, Teams chats/channels, meeting transcripts, and files.
- **Draft** emails, recaps, meeting notes, documents, Teams posts.
- **Gather & compile** — pull from several sources into one document or summary.
- **Coordinate** — schedule meetings, organize a day, chase open items (drafts the chasers).
- **Classify & route** — triage incoming requests into a list, label them, draft acknowledgments.
- **Extensible** via plugins/connectors from the M365 app store (specialized skills or external
  data) — but custom/third-party skills are **not** Microsoft-validated; review their output.

## What it can't do / hard limits

- **Files:** OneDrive/SharePoint only — **no local-device files**; can't read **encrypted** files
  (even if you have access); **can't delete** files/folders; attachments must be **< 200 MB**.
- **Scope:** operates inside the M365 ecosystem and **strictly within your existing permissions** —
  it opens no new access paths.
- **Identity:** runs under **your own user identity**, not a separate agent account — so every
  action it takes is attributed to you (a segregation-of-duties point, see guardrails).
- **Not a calculator of record:** it can manipulate text and orchestrate, but you must never let it
  **originate or compute financial numbers** that feed reporting. That's our rule, reinforced by the
  fact that custom skills and model output aren't guaranteed correct.

## 🚩 Residency reality (the gating question)

- Cowork **runs on Anthropic models**, available only in Anthropic-supported regions.
- Per Microsoft's data-protection documentation and launch reporting, **Anthropic models are
  currently out of scope for the EU Data Boundary** and in-country processing commitments.
- Where data-residency enforcement is available for Copilot, it adds **~10% to credit consumption**.
- **Implication for us:** our charter requires EU residency for work data. Until tenant admin/
  security confirm how Cowork processing is handled for our EU tenant, **no real Controlling data
  goes into Cowork** — tests run on low-sensitivity synthetic/coordination content only.

## Cost model

- **Usage-based** — Copilot Credits, list price **~$0.01/credit**. Rough task tiers: light **$1–3**,
  medium **$4–7**, heavy multi-output **$7+**.
- **Not** included in the base M365 Copilot licence — billed **separately** on usage.
- **Deadline:** tenants without usage-based billing configured **lose Cowork access after
  1 Jul 2026**. Confirm billing is set up if the team intends to keep it.

## What this means for our use cases

The capabilities map cleanly onto **coordination and communication toil** — summarizing, drafting,
gathering, chasing, triaging — which is exactly the steer (recurring team work + lifting manual work
off management). The limits push us *away* from anything involving the books, local files, or
unattended action. Every viable use case therefore looks the same shape: **Cowork does the legwork →
a human approves → numbers (if any) come from a deterministic source.** See the use-case catalog.

## Sources

- [Cowork overview — Microsoft Learn](https://learn.microsoft.com/en-us/microsoft-365/copilot/cowork/)
- [Cowork common questions (limits) — Microsoft Learn](https://learn.microsoft.com/en-us/microsoft-365/copilot/cowork/cowork-faq)
- [Manage Cowork / admin & governance — Microsoft Learn](https://learn.microsoft.com/en-us/microsoft-365/copilot/cowork/cowork-admin-governance)
- [Cowork is now generally available — M365 Blog](https://www.microsoft.com/en-us/microsoft-365/blog/2026/06/16/copilot-cowork-is-now-generally-available/)
- [Data, privacy & security for M365 Copilot — Microsoft Learn](https://learn.microsoft.com/en-us/microsoft-365/copilot/microsoft-365-copilot-privacy)
- Pricing/credits coverage (third-party, verify): [Quisitive](https://quisitive.com/copilot-cowork-pricing-2026-how-usage-based-billing-works/), [HBS](https://www.hbs.net/blog/copilot-cowork-available-now)
