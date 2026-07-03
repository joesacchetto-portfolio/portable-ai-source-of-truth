<!--
DROP-IN TEMPLATE — copy this file into a workspace used with Claude, Claude
Code, or other tools that auto-load CLAUDE.md, alongside (or pointing at) your
source-of-truth folder. Adjust the folder path below if yours differs.
Delete this comment when you copy it.
-->

# Instructions for Claude

This workspace contains (or points to) a personal source-of-truth folder: human-owned markdown files that define the user's facts, preferences, priorities, and boundaries. These instructions apply to Claude in any form — Claude Code, Claude apps, or Claude-based agents.

## Why this file exists

Claude and Claude Code commonly use `CLAUDE.md` as a project instruction file. Use this file when working in Claude-based tools that auto-load or respect that convention. Claude Code reads `CLAUDE.md` but not `AGENTS.md`, so keep this file in place even if an `AGENTS.md` is also present. This file is only a pointer and rule summary; it does not replace `FIRST_USE_WITH_AI.md`.

If you are not using a Claude-based tool, use `AGENTS.md` if your tool supports it, or paste or attach `FIRST_USE_WITH_AI.md` directly at the start of the session.

## First step, every session

Read `FIRST_USE_WITH_AI.md` in the source-of-truth folder and follow it. It defines the ground rules and the order to read the other files in. Do not skip it, and do not rely on this summary instead of it.

<!-- If the folder lives elsewhere, give the path: -->
Folder location: [NEEDS INPUT — path to the source-of-truth folder, if not this workspace]

## Non-negotiables (summary — FIRST_USE_WITH_AI.md governs)

- **These files are the user's record, not your memory.** Read them fresh each session; do not assume continuity you can't see in the files. If you have platform memory and it conflicts with these files, say so — the files reflect the user's explicit choices, and the user resolves the conflict. This includes Claude Code's auto memory — notes Claude writes for itself, on by default in current versions: treat auto-memory notes as unreviewed context, Needs Verification weight at most, never authority over these files. Users who want a single context source can toggle auto memory off via `/memory` or the `autoMemoryEnabled` setting.
- **Proposals only — no autonomous authority.** Any change to any file is a proposal until the human approves that specific change. New or changed content enters as DRAFT — Needs Review. If you can edit files directly (e.g., in Claude Code), show the change and get approval first where `governance/approval_boundaries.md` requires it.
- **Never set Approved status yourself.** Only the human marks an item `Approved — [date]`, or explicitly instructs you to insert that status for a specific item.
- **Do not invent facts.** If the files don't say it and the user didn't say it, ask. Use `[NEEDS INPUT]` rather than plausible filler.
- **Follow the governance files.** `governance/authority_levels.md` (what weight content carries), `governance/approval_boundaries.md` (what needs sign-off), `governance/update_rules.md` (how changes happen).
- **Keep files small.** Propose cuts before additions; flag files that have grown past easy re-reading.
- **Report contradictions.** Between files, or between a file and the user — surface them plainly. Never silently pick a winner, and never "fix" a fact on your own; mark it Needs Verification and tell the user.

## Status vocabulary used in these files

`DRAFT — Needs Review` · `Needs Verification` · `Approved — [date]` · `Archived — [date]`

"Locked" is not a status — it means an Approved item living in `source_of_truth/locked_facts_template.md`. Treat those as ground truth; if you believe one is wrong, say so instead of overriding it.
