# Workflow: Transcript to Approved Updates

Use this when you have a transcript — a meeting recording's text, a chat log, a call summary — and want its contents reflected in your framework without letting errors in.

**The risk this workflow manages:** transcripts are where bad context sneaks in. Summaries drift from what was said, assistants invent connections between meetings, and one person's passing worry becomes a "fact" that haunts every future session. Every step below exists to stop one of those.

## Steps

**1. Give the assistant the transcript and this instruction:**

> Summarize this transcript. Rules: only what was actually said — every point must trace to a specific statement in the transcript. Do not add background knowledge, do not connect this to other meetings or prior context unless the transcript itself does, and do not infer what people "really meant." Mark anything ambiguous as ambiguous. Attribute views to the people who expressed them; a concern someone raised is that person's concern, not a fact. If no transcript is attached to this instruction, say so and stop — never summarize assumed or reconstructed content. If what I gave you is a prompt requesting future analysis rather than a record of what happened, summarize the request itself — constraints, decisions needed, open questions — not the outcome of work that hasn't happened.

**2. Check the summary against the transcript.** Spot-check the points that matter most. Anything you can't trace to the transcript gets cut or marked `Needs Verification`.

**3. Ask the assistant to propose framework updates — as a list, not as edits:**

> Based on the approved summary, list any proposed updates to my framework files. For each: the file, the exact text to add or change, and the status it would enter at (always DRAFT — Needs Review). Propose only; do not edit.

**4. Filter the proposals hard.** For each one, ask:

- Is this durable, or just what this meeting felt like? Temporary concerns and one-off moods go nowhere — or at most into `current_working_context` where they'll be replaced.
- Is it a decision? Then it goes to the decision log, with the transcript as its rationale source.
- Is it a fact candidate for locked facts? Almost never from one transcript. Route it to `Needs Verification` at best, and confirm it independently before ever approving it there.
- Is it about another person? Apply `docs/privacy_and_review_warnings.md` — most of it shouldn't be stored.

**5. Approve, then apply.** Accepted changes are applied exactly as approved, entering as DRAFT — Needs Review until you mark the specific items `Approved — [date]` per `governance/update_rules.md`. Everything the assistant produced along the way is a proposal until you've done this.

## Quick rules of thumb

- If it isn't in the transcript, it doesn't come out of this workflow.
- No transcript in hand means no summary — the workflow starts when the source exists.
- One meeting changes `current_working_context`; it takes much more to change locked facts.
- When a summary sounds smoother than the meeting actually was, that smoothness is usually invention.
