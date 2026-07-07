# Privacy and Review Warnings

Read this before you put anything about yourself or your work into these files.

## Warning 1: Plain text is not safe for secrets

These files are ordinary text. They are not encrypted, not access-controlled, and — most importantly — **whatever is in them gets sent to an AI provider every time you share them in a session.**

Never put these in any file in this folder:

- Passwords, API keys, tokens, or credentials of any kind
- Financial account numbers or payment details
- Health or medical information (yours or anyone's)
- Government ID numbers
- Other people's personal information — names tied to private details, contact info, performance issues, salaries
- Anything covered by an NDA, attorney–client privilege, or your employer's confidentiality rules
- Anything you would not paste into a chat window with a third-party service — because that is exactly what you'll be doing

If you need the AI to know "I have a vendor contract with strict terms," write that. Don't paste the contract.

**Rule of thumb:** write about your work at the level you'd use with a competent new colleague on day one — before they've signed anything.

## Warning 2: Where you store the folder matters

A synced drive shared with your team is not private. A public git repo is public. Before you fill in the templates, decide where this folder lives and who can see it. If you use git, check what you're committing before you push.

## Warning 3: AI-generated content starts as draft — always

When an AI assistant fills in the live files from the starter templates, or proposes updates, that content is a **draft**, not a fact. AI assistants guess plausibly. They will state your preferences more strongly than you hold them, round your history to a cleaner story, and fill gaps with invention.

So this framework uses a simple status convention:

- Everything an AI writes enters as **DRAFT — Needs Review**.
- Only **you** move something to **Approved** — after actually reading it.
- An AI assistant may never mark content as Approved, and may never move content into locked facts. Not on your instruction to "just approve it all," either — the reading is the point. (Exception: after you explicitly confirm a specific item, you may tell the assistant to insert that exact `Approved — YYYY-MM-DD` status for that item. See `governance/update_rules.md`.)

If you skip review, you will end up with a source-of-truth folder that confidently misleads every future session. That is worse than no folder at all.

## Warning 4: AI memory is useful input, not truth

If you ask an AI assistant to draft a rough Context Seed from its memory or prior chat history, treat that output as unreviewed draft material. AI memory can be stale, incomplete, overconfident, or mixed with context that no longer applies. It can also surface details you do not want stored in plain text.

Before splitting a rough seed into files, read it yourself. Delete sensitive material, correct wrong claims, and mark uncertain items as `[NEEDS VERIFICATION]` or `[NEEDS INPUT]`. The draft seed normally lives at `imports/context_seed.md`; that file may contain the most sensitive unreviewed material in the folder. Nothing from AI memory becomes part of your source of truth until you review and approve the specific item.

## Warning 5: Review is recurring, not one-time

Facts go stale. Priorities shift. A file you approved earlier can quietly become wrong. Run `prompts/04_audit_for_drift.md` periodically, on a schedule you choose, and re-read any file before relying on it for something important.

## Warning 6: You can always remove things

Nothing here is permanent. If you realize something sensitive slipped in, delete it. (If the folder is in git, note that history keeps old versions — you may need to clean history or rotate anything exposed.) When in doubt, leave it out: a smaller, safer file beats a complete, risky one.
