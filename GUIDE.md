# How to use your consulting team

This is the user manual for the workspace. Read it once top to bottom; after that, the
[Quick reference](#quick-reference) at the bottom is all you'll need.

---

## The 30-second mental model

You have a **six-person consulting team** that lives in this repo. You open Claude Code here and
talk to them. They design finance automations, write the prompts your work Copilot will run, and
hand you build instructions.

Two rules shape everything:

1. **Two environments.** This repo is on your **personal device** — the team works with *mock data
   only*. The real building and running happens **at work**, by you, with your approved tools.
   Because the repo isn't reachable from your work machine, everything the team produces is built
   to be **carried across by hand** (read from a second screen, typed in at work).

2. **The team never touches real data or real systems.** Not SAP, not BlackLine, not one real row.
   You bring them the *shape* of a problem (column names, process steps, anonymized samples); they
   give you back designs and instructions.

```
   YOU + TEAM (here)                    YOU + work Copilot (at work)
   design on mock data   ──carry──▶     build & run on real data
        ▲                                        │
        └──────────── report back ◀──────────────┘
```

---

## Starting a session

Open Claude Code in this folder. That's it — the charter (`CLAUDE.md`) loads automatically, so the
team already knows your role, your tools, your constraints, and the projects in flight. You never
re-explain.

A good opening line is just plain English:

- *"Where are we?"* — get oriented (the team reads the project briefs).
- *"I want to speed up my intercompany rec."* — start a new piece of work.
- *"Review this flow for me: …"* — get a critique.

Or use a **mode command** to be explicit about what you want (next section).

---

## The four modes

Modes set the team's behavior. Invoke them with a slash command **or** plain words — both work.

| Mode | Command | Plain words | Use it when… |
|---|---|---|---|
| **Brainstorm** | `/brainstorm <topic>` | "brainstorm: …" | You want lots of ideas, fast, no filtering. |
| **Plan** | `/plan <idea>` | "plan this: …" | An idea is worth designing properly. Runs the full workflow. |
| **Build** | `/build <thing>` | "build mode: …" | A design is ready and you want the transfer-ready artifact. |
| **Review** | `/review <thing>` | "review mode: …" | You already have a flow/script/prompt and want it critiqued. |

**Brainstorm** gives you 10–15 ideas, each tagged with which specialist would own it. Keepers can
go to `projects/BACKLOG.md`.

**Plan** is the workhorse. It runs the team's five-step workflow:
1. **Discovery** — they ask you sharp questions first (volumes, sources, who does what, where it
   hurts). *They will not design on assumptions* — answer these.
2. **Options** — 2–3 approaches, simplest first, with honest trade-offs including transfer cost.
3. **Recommendation** — one option, with reasoning.
4. **Execution plan** — milestones tagged `[HERE]` (done in this repo) or `[AT WORK]` (you do it),
   with human checkpoints and rollback.
5. **Compliance sign-off** — the reviewer gives a verdict before anything is final.
   Ends by writing a **project brief** in `projects/`.

**Build** produces the actual artifact you carry to work (a prompt card, a build recipe, or a code
spec — see [the transfer loop](#the-transfer-loop)) and ends with a transfer checklist plus the
at-work checks you'll run.

**Review** critiques something you already have. Paste it in (anonymized). You get: what's solid,
findings by severity (Blocker / Major / Minor), simplest fix first, and a compliance pass.

> If `/review` ever clashes with a built-in review command, type **"review mode:"** instead.

---

## The six specialists

The team self-routes most of the time, but you can summon anyone by name — *"ask the architect…"*,
*"have compliance look at this…"*.

| Specialist | Summon them for |
|---|---|
| **architect** | The overall design. Which tool for the job, how pieces fit, how it scales to 80+ entities. Start here for anything new. |
| **power-platform-engineer** | Hands-on builds: Power Automate flows, Power Apps, Office Scripts, SharePoint, connectors, and Copilot Studio plumbing. Gives you exact click-by-click recipes. |
| **copilot-prompt-engineer** | Anything your **work Copilot** runs: M365 chat prompts, Excel prompts, Copilot Studio instructions. Owns the `prompts/` library. |
| **python-data-engineer** | Reconciliation engines and data work. Delivers spec + tests so you don't retype code at work. |
| **compliance-reviewer** | The SOX auditor. Has **veto power** — nothing is "final" without their sign-off. Pull them in early, not just at the end. |
| **strategy-consultant** | What to build first, how to pitch it, rollout plans, and how each project builds your AI-Finance-Analyst positioning. |

You rarely need to think about this — describe your problem and the right person shows up. Naming
them is just a shortcut when you know who you want.

---

## The transfer loop

This is the part that makes the workspace different from a normal project, so it's worth
understanding well.

**The problem:** the team designs here, but you can't open this repo at work. So a 300-line script
or a screenshot is useless — you'd have to retype it perfectly. Everything is therefore shaped to
**survive the air gap**. There are three artifact types, and the team picks the right one:

| Artifact | What it is | How you carry it |
|---|---|---|
| **Prompt card** (`prompts/`, `deliverables/`) | One screen of text for your work Copilot. | Type it once at work, then *save it there* (saved prompt / Studio instruction). |
| **Build recipe** (`deliverables/`) | Numbered steps with a checkpoint after each ("you should now see…"). | Follow it on the work machine, step by step, from a second screen. |
| **Code spec + tests** (`deliverables/`) | A build spec plus acceptance tests (input → expected output). The actual reference code stays *here*. | At work, have Cursor/Copilot **regenerate** the code from the spec, then run the acceptance tests to prove it matches. You never retype the code. |

**Every artifact carries a status:** `draft → transferred → verified-at-work`. That's how you know
what's been proven on real data and what hasn't. (This is why the two starter prompt cards are
marked `draft` — they're written and ready, but not yet tested at work.)

**The loop in practice:**
1. **Design here** on mock data until it's boringly reliable.
2. **Carry it across** using the transfer checklist the team gives you.
3. **Run it at work**, starting with the artifact's verification checks (often a *known-answer
   test* — data where you already know the right output).
4. **Report back** — "worked", or "failed like this" (anonymized). The team tunes it and the
   project brief's transfer log gets updated.

---

## Data hygiene — read this once, never forget it

This repo is on a personal device and on GitHub. **Zero real TD SYNNEX data here — in files *or*
in chat.**

✅ **Fine to bring:** process descriptions, column names and schemas, screenshots *described in
words*, and synthetic samples — `Entity A` / `E001`, `Vendor 0001`, `Customer C-0042`, invented or
scaled balances, made-up dates.

🚫 **Never:** real customer/vendor/employee names, real balances or volumes you could trace to an
entity, internal URLs or system IDs, or anything copied from a real SAP/BlackLine/Workiva extract —
not one row, not even "just in chat to explain it".

If you accidentally paste something real, the team will **stop and help you anonymize it** before
going further. When in doubt, change the numbers and names — the *shape* is all the team needs.

---

## A worked example, end to end

Here's the whole machine working on one realistic task. Follow the flow, not the specifics.

**You type:** `/plan speed up my intercompany reconciliation`

**Discovery** — the team asks: how many entity pairs, what volumes, where does the data come from
(SAP export? which columns?), what match rules do you apply today, who certifies in BlackLine?
*You answer with anonymized facts.*

**Options** — the architect lays out three, simplest first:
- A Power Query template you refresh each month *(lowest effort, least scalable)*.
- A Python tiered-matching engine — exact → composite key → amount-within-tolerance *(scales to all
  pairs, strongest audit trail)*.
- An Office Script + flow hybrid.

…each with honest trade-offs, including what it costs to carry across the air gap.

**Recommendation** — the Python engine, because it scales across entity pairs and leaves a clean
control trail. **Compliance** signs off *with conditions* (control totals on every run, exceptions
go to a human, run log retained). A **brief** is written to `projects/02-account-reconciliations.md`.

**Later, you type:** `/build the matching engine`

The python-data-engineer builds it *here against mock data* and hands you, in
`deliverables/02-account-reconciliations/`:
- a **spec** (`spec-matching-engine.md`) precise enough to regenerate the code from,
- **acceptance tests** with golden input/output files,
- the **reference implementation** (stays here as proof),
- a **transfer checklist**: what to carry, in what order.

**You go to work and:**
1. Open Cursor, paste the spec, let it generate the code.
2. Run the acceptance tests → they pass → the regenerated code provably matches what was proven here.
3. Run it on one real entity pair as a known-answer test.

**You come back and say** "passed on the pilot pair." The brief's transfer log flips that artifact
to `verified-at-work`, and the team plans the rollout to the rest.

That's the loop. Every project rides it, usually more than once.

---

## Project memory & picking up later

The team's memory lives in `projects/` — one brief per project. Each brief holds the decisions made
(and *why*), open questions, risks, the compliance verdict, and the transfer log.

- **To resume anything:** just ask *"where are we on reconciliations?"* — the team reads the brief.
- **Before a session ends**, the team updates the brief automatically. You don't have to manage it.
- **New ideas** that aren't ready for a full plan go to `projects/BACKLOG.md`.

This is why you never lose context between sessions, even weeks apart.

---

## Quick reference

**Modes**
```
/brainstorm <topic>   lots of ideas, no filtering
/plan <idea>          full workflow → project brief
/build <thing>        transfer-ready artifact + checklist
/review <thing>       critique (technical + compliance)
```

**Summon a specialist:** *"ask the architect…"*, *"have compliance review this…"*

**Folders**
```
CLAUDE.md         the charter (loads every session)
GUIDE.md          this file
projects/         one brief per project + BACKLOG.md  ← team memory
deliverables/     what you carry to work (per project)
prompts/          prompt cards for your work Copilot
mock-data/        synthetic test data + generators
local/            scratch; never committed
```

**The three transfer artifacts:** prompt card (type & save at work) · build recipe (follow
step-by-step) · code spec + tests (regenerate at work, verify with tests).

**Status lifecycle:** `draft → transferred → verified-at-work`.

**The one hard rule:** no real company data here, ever — anonymized samples only.

---

## Your first week (suggested)

1. **Map what's already live.** Start `01-automation-inventory` — bring an anonymized list of the
   flows/scripts running at work today. This stops the team from designing something that
   duplicates or breaks an existing one. *"Let's work on the automation inventory."*
2. **Prove the loop on something tiny.** Pick one painful manual step and run it through `/plan`
   then `/build`, so you experience the full design→transfer→verify cycle once on low stakes.
3. **Validate the two starter prompt cards.** Ask the team to generate a mock dataset, dry-run
   `chat-close-status-note` and `excel-anomaly-scan` here, then carry them to work and move them to
   `verified-at-work`.

After that, point the team at whatever's costing you the most hours.
