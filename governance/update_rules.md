# Update Rules

This file defines how the files in this folder may be changed, reviewed, and status-marked — by you and by any AI assistant working with you.

## Statuses

Every substantive item (a fact, rule, preference, priority, or decision) carries one status:

- **DRAFT — Needs Review**: new or changed content that no human has confirmed yet. All AI-generated material starts here, with no exceptions.
- **Needs Verification**: uncertain — the human saw it and wasn't sure it's (still) right, or an assistant flagged it with specific stated evidence. It stays flagged, carrying no reliable authority, until the human resolves it.
- **Approved — [date]**: the human read this specific item and confirmed it. Only a human can apply this status.
- **Archived — [date]**: kept for history, no longer active. See `authority_levels.md`.

"Locked" is not a separate status — it's an Approved item living in `source_of_truth/locked_facts_template.md`, which gets the strictest review (see below).

Use ISO-style dates in statuses: YYYY-MM-DD.

## Who may change what

**Humans** may change anything, any time. It's your folder. (One habit worth keeping even for yourself: when you meaningfully change an Approved item, re-date it.)

**AI assistants** may:

- Draft new content, entering at DRAFT — Needs Review.
- Propose edits to existing content, shown as before/after, applied only on approval.
- Apply the specific edits a human approves, exactly as approved.
- Update `core_context/current_working_context_template.md` to reflect what the human said in the current session — quoting, not interpreting — entering at DRAFT — Needs Review (see `approval_boundaries.md`, "Allowed without sign-off").
- Flag issues (staleness, contradictions, privacy risks) without editing.
- Append a `Needs Verification` flag to any item — locked facts included — given specific stated evidence it may be wrong. Flagging is one-way: assistants never remove or downgrade flags, change the item's content, or apply any other status.

**AI assistants may never:**

- Mark anything Approved, or move anything into `source_of_truth/locked_facts_template.md` — even if instructed to "approve it all." New or AI-generated material becomes Approved only after a human reads that specific item and confirms it. (One exception: inserting the status after the human confirms a specific item and gives an explicit item-level instruction — see step 4 below.)
- Edit governance files, locked facts, or approved content without item-level sign-off (see `approval_boundaries.md`). Exceptions, both per that file's "Allowed without sign-off" list: adding DRAFT entries under its "My additional sign-off items" section, and appending `Needs Verification` flags.
- Delete content silently. Deletions are proposed; the human deletes or approves the deletion.

## How a change happens

1. **Propose.** State the file, the section, and exact before/after text.
2. **Show the landing level.** New material enters as DRAFT — Needs Review, at Working Assumption authority or lower. Nothing enters as a Locked Fact directly.
3. **Human decides.** Approve, edit, or reject. No response is not approval.
4. **Apply and mark.** Apply exactly what was approved. The human sets the status and date. If the assistant can edit files directly, it may insert the status only when the human gives an explicit item-level instruction such as: "Mark this exact item Approved — YYYY-MM-DD."
5. **Log if it matters.** Decisions that future sessions should know about go in `decisions/decision_log_template.md`.

## Special case: locked facts

Changes to `source_of_truth/locked_facts_template.md` get the strictest handling: one fact at a time, explicit confirmation per fact, and a decision-log entry when a locked fact is added, changed, or retired. If a session surfaces evidence that a locked fact is wrong, the assistant appends a `Needs Verification` flag (stating the evidence) and the human resolves it — the fact doesn't get "fixed" in place.

## Keeping files usable

Prefer editing over appending; these files should stay current, not accumulate. Move superseded material to an Archive section rather than deleting it, unless it is a privacy risk — privacy risks get deleted. If a file has grown past what you'd willingly re-read, that's the signal to prune.
