# Example: A Completed Framework (Fictional Project Manager)

> **This example is entirely fictional.** "Dana" and everything else below were invented for this file. Nothing here is true, and none of it should be copied into your own framework as fact. It exists to show what the templates look like *filled in* — the level of detail, the status marks, and how the pieces fit together. Your real framework will live across the separate template files, not in one document like this.

The fictional setup: Dana is a fictional project manager at a fictional mid-sized software company, coordinating rollout of an internal request-tracking tool.

---

## From: core_context/operating_rules_template.md

Status: Approved — 2026-05-02

- Default to short answers; I'll ask when I want depth. — Approved — 2026-05-02
- Show me an outline before drafting anything longer than a page. — Approved — 2026-05-02
- When I ask for options, give exactly three, with your recommendation first. — Approved — 2026-05-02
- Push back once if you think I'm wrong, clearly, then follow my call. — Approved — 2026-05-02

## From: core_context/do_not_do_template.md

Status: Approved — 2026-05-02

- Never present unreviewed or invented content as established fact. — Approved — 2026-05-02
- Never send, post, or share anything externally on my behalf. — Approved — 2026-05-02
- Never commit me to dates in a draft — write "target," never "deadline," until I confirm. — Approved — 2026-05-02
- Never assume department heads report to me. I coordinate them; I don't manage them. — Approved — 2026-05-02

## From: core_context/current_working_context_template.md

Status: Approved — 2026-06-24
Last updated: 2026-06-24

### Active work

- **Tool rollout — Phase 2 (Operations dept)** — training sessions done; adoption tracking in progress — next: draft the adoption summary for the steering group
- **Vendor renewal for the analytics add-on** — comparing two quotes — next: send comparison to finance contact

### Waiting on

- Facilities headcount numbers for the Phase 3 plan — requested 2026-06-19. — Needs Verification (may have arrived in the shared inbox; check before chasing)

### Current constraints

- Change freeze during the fiscal-year close: no configuration changes to the tool until the freeze lifts.

## From: source_of_truth/locked_facts_template.md

- The tool we are rolling out is an internal request tracker. It is not customer-facing. — Approved — 2026-05-02
- "Launch" in this project means a department starts daily use, not the software install date. — Approved — 2026-05-02
- I own the rollout schedule and training plan. Budget approval sits with the steering group, not me. — Approved — 2026-05-02
- The Phase 1 department (Customer Support) is the reference case other departments are told about. — Approved — 2026-05-20

## From: source_of_truth/current_priorities_template.md

Status: Approved — 2026-06-10

1. **Phase 2 adoption actually sticking** — why it's first: Phase 3 approval depends on Phase 2 numbers; a stalled Phase 2 stalls everything.
2. **Keeping the steering group informed early** — why it's above the rest: surprises cost more trust than bad news does.
3. **Vendor renewal decision** — matters, but has a clear process and a hard date; it mostly needs to not be forgotten.

- When 1 and 2 conflict: protect adoption work and tell the steering group what got delayed.
- Explicitly not a priority right now: evaluating replacements for the tool. Raised occasionally; parked until after Phase 3. — Approved — 2026-06-10

## From: decisions/decision_log_template.md

### [2026-06-12] — Phase 3 scope excludes the field team

- Decision: Phase 3 covers office departments only; the field team gets its own later phase.
- Rationale: Field workflows differ enough that bundling them risked both schedules.
- Status: Approved — 2026-06-12
- Affects: current_working_context (Phase 3 plan), current_priorities (no change to ranking)
- Review notes: Revisit if the field team's tooling budget is approved earlier than expected.

### [2026-04-28] — Weekly status format: one page, three headings

- Decision: Status updates to the steering group use one page: Done / At risk / Decisions needed.
- Rationale: The previous format buried the asks; two members said they'd stopped reading it.
- Status: Archived — 2026-06-12 (superseded: steering group now wants "Decisions needed" first; see decision of 2026-06-12 in the full log — not shown in this condensed example)

## From: decisions/approved_phrasing_template.md

- Phrasing: "Phase 2 is tracking against the revised plan agreed in May, not the original January plan."
  - Use when: any status communication that mentions Phase 2 timing.
  - Status: Approved — 2026-06-10

## From: decisions/rejected_patterns_template.md

- Pattern: calling adoption issues "user resistance."
  - Why rejected: it frames colleagues as the problem; Dana wants issues described by cause ("the approval step adds clicks"), not by blame.
  - Status: Approved — 2026-05-20
- Pattern: adding an executive summary to documents that didn't ask for one.
  - Why rejected: steering group reads the one-pager itself; a summary of one page reads as padding.
  - Status: Approved — 2026-05-02

---

## What to notice in this example

- **Everything carries a status**, and the dates differ — approval happened over multiple sittings, not in one batch.
- **One item is Needs Verification** (the facilities headcount, under Waiting on) — Dana saw it, wasn't sure it was still current, and marked it rather than deleting or trusting it.
- **One item is Archived** (the old status format) — superseded by a new decision, kept with a pointer instead of being rewritten.
- **Locked facts are few and boring.** Four short lines — what the tool is, what "launch" means, what Dana owns, what the reference case is. That's the right size.
- **The "why" fields do the work.** Priorities explain their ranking; rejections explain their reason. That's what lets an assistant make good judgment calls instead of pattern-matching.
