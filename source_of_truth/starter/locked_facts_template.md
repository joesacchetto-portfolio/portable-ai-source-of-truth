# Locked Facts

<!--
TEMPLATE — replace the placeholders with your own facts, then delete these
comments.

This is the strictest file in the folder. A fact belongs here only if ALL of
these are true:

  1. It is stable — not expected to change without a deliberate event.
  2. You have read the exact wording and marked it Approved — [date].
  3. It matters — an assistant getting it wrong would cause real problems.

Everything here is treated as ground truth (Locked Facts authority — see
governance/authority_levels.md). Assistants must not contradict, "correct," or
reword these. That power cuts both ways: a wrong locked fact will confidently
poison every session, so keep this list short and keep it right.

Not sure it's stable? It goes in core_context/current_working_context.md
instead. Not sure it's true? Mark it Needs Verification — an item that has not
been confirmed carries NO locked-fact authority until you resolve it.

Rules (from governance/):
- AI-generated additions start as DRAFT — Needs Review. Only you move an item
  to Approved — [date], one fact at a time.
- Adding, changing, or retiring a locked fact gets a decision-log entry.
- If evidence suggests a fact is wrong, it gets marked Needs Verification —
  never silently "fixed."
-->

<!-- Format: one fact per line, exact wording, own status per fact.
     Only facts marked Approved — [date] carry locked-fact authority. -->

## Role and scope

- [NEEDS INPUT — e.g., "I am the implementation lead for [product], responsible for delivery, not for pricing decisions."] — DRAFT — Needs Review

## Work facts assistants must not get wrong

<!-- The details assistants repeatedly misstate: names of systems, what a term
     means in your org, what you do and don't own. -->

- [NEEDS INPUT] — DRAFT — Needs Review
- [NEEDS INPUT] — DRAFT — Needs Review

## Definitions

<!-- Terms that mean something specific in your context, so assistants stop
     using the generic meaning. -->

- [NEEDS INPUT — e.g., "'Launch' in my context means internal go-live, not public release."] — DRAFT — Needs Review

---

## Archive

<!-- Retired facts move here, marked Archived — [date], with a one-line reason.
     Archived facts carry no authority. -->

- [empty]
