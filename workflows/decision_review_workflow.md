# Workflow: Reviewing an AI-Proposed Change

Use this whenever an assistant proposes changing anything in your framework — during a session, after a transcript summary, or from a drift audit. It's short on purpose: the point is that you actually run it every time rather than waving changes through.

**The rule underneath it:** every AI proposal is exactly that — a proposal. Nothing takes effect until you've seen the specific change and said yes to it (`governance/update_rules.md`).

## Steps

**1. Get the proposal in reviewable form.** A proper proposal names:

- **File** — which file changes.
- **Exact text** — before and after, not a paraphrase.
- **Authority level** — what weight the content would carry (`governance/authority_levels.md`). New material enters at Working Assumption or lower — never directly as a locked fact.
- **Status** — what it enters as (always DRAFT — Needs Review for new/changed content).

If the assistant gave you less than this, ask for the missing pieces before judging anything.

**2. Check the boundary.** Does the change touch anything in the always-requires-sign-off list — approved content, locked facts, governance files, deletions, anything about other people? (`governance/approval_boundaries.md`.) If yes, slow down; those get item-level scrutiny.

**3. Judge the content.** Three questions:

- **True?** Not "plausible" — can you personally vouch for it? If not: `Needs Verification`, not approval.
- **Durable enough for its target file?** A current-work detail proposed for locked facts is in the wrong place, even if true. Re-route it.
- **Worth storing?** Every line in the framework is something future sessions will act on. If it wouldn't change an assistant's behavior, decline it — smaller stays truer.

**4. Decide: accept, edit, re-route, or reject.** Partial acceptance is normal — take the fact, cut the editorializing. The assistant applies exactly what you accepted, nothing more.

**5. Mark status yourself.** You set `Approved — [date]` on items you've confirmed (or give an explicit item-level instruction like "Mark this exact item Approved — YYYY-MM-DD"). If the change was significant — anything touching locked facts, or reversing a past decision — add a decision-log entry.

## Red flags worth a hard stop

- A proposal that bundles many changes into one yes. Unbundle it.
- A proposal to "clean up" or "clarify" approved content — rewording changes meaning. Diff it word by word.
- A proposal whose rationale is what you said casually in this session. You were thinking out loud; make sure you actually meant it.
