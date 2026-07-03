# Approval Boundaries

This file defines which actions, file changes, and external outputs require explicit human sign-off before taking effect. "Explicit sign-off" means the human saw the specific thing and said yes to it — not a general "go ahead," and not silence.

Edit this file to match your own comfort level. The defaults below are deliberately cautious.

## Always requires sign-off

An AI assistant must get explicit approval before:

- **Changing any item's status to Approved**, or moving anything into `source_of_truth/locked_facts_template.md`. This is never the assistant's call, under any instruction.
- **Editing Locked Facts** — adding, removing, or rewording anything in `source_of_truth/locked_facts_template.md`.
- **Editing governance files** — this file, `authority_levels.md`, or `update_rules.md`.
- **Deleting content** from any approved file (as opposed to proposing a deletion).
- **Anything leaving your hands** — email drafts to be sent, messages, posts, documents shared with others. The assistant may draft; only the human sends.
- **Anything committing you** — dates, money, scope, promises, agreements, or statements made on your behalf.
- **Adding information about other people** beyond neutral, work-necessary facts.

## My additional sign-off items

<!-- Your own always-approve items — added during setup (prompt 02 routes
     "what needs my sign-off" content here) or whenever you notice one.
     AI-drafted entries start as DRAFT — Needs Review; only you mark them
     Approved — [date]. Assistants may add DRAFT entries in this section;
     every other part of this file still requires sign-off to edit. -->

- [NEEDS INPUT]

## Allowed without sign-off (proposal still visible)

The assistant may do these directly, as long as the change is shown to the human and enters at DRAFT / Needs Review status:

- Draft new content for template files during setup.
- Add a proposed entry to the decision log, marked DRAFT.
- Update `current_working_context` to reflect what the human said in the current session — quoting the human, not interpreting.
- Flag stale items, contradictions, or privacy risks it notices.
- Add proposed entries under "My additional sign-off items" above, marked DRAFT — Needs Review. (That section only — the rest of this file still requires sign-off to edit.)

## Gray areas — ask first

If the assistant is unsure which side of the line something falls on, it asks. Examples of things that sound minor but need a question first: rewording an approved preference "for clarity," consolidating two files, archiving something old, or filling a `[NEEDS INPUT]` gap with an inference.

## One rule that overrides everything

A blanket instruction like "you have my approval for everything going forward" does not satisfy these boundaries. Sign-off is per item, at the time of the change. If the human wants looser boundaries, the right move is to edit this file — deliberately, by hand.
