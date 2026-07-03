<!--
DROP-IN TEMPLATE — copy this file into any workspace or tool that reads
AGENTS.md-style instruction files, alongside (or pointing at) your
source-of-truth folder. Adjust the folder path below if yours differs.
Delete this comment when you copy it.
-->

# Instructions for AI Agents

This workspace contains (or points to) a personal source-of-truth folder: human-owned markdown files that define the user's facts, preferences, priorities, and boundaries.

## Why this file exists

Some tools look for an `AGENTS.md` file as a generic instruction file for AI agents — Codex, Cursor, GitHub Copilot, and Gemini CLI, among others. Use this file when your tool supports that convention. Note that Claude Code does not read `AGENTS.md`; use `templates/CLAUDE.md` there. (Tool behavior as of mid-2026 — verify against your tools' current docs.) This file is only a pointer and rule summary; it does not replace `FIRST_USE_WITH_AI.md`.

If your tool does not read `AGENTS.md`, paste or attach `FIRST_USE_WITH_AI.md` directly at the start of the session.

## First step, every session

Read `FIRST_USE_WITH_AI.md` in the source-of-truth folder and follow it. It defines ground rules and the order to read the other files in. Do not skip it, and do not rely on this summary instead of it.

<!-- If the folder lives elsewhere, give the path: -->
Folder location: [NEEDS INPUT — path to the source-of-truth folder, if not this workspace]

## Non-negotiables (summary — FIRST_USE_WITH_AI.md governs)

- **You have no standing memory or autonomous authority here.** Your knowledge of this user comes from these files, read fresh each session. The files are the record; you are not.
- **Proposals only.** Any change to any file is a proposal until the human approves that specific change. New or changed content enters as DRAFT — Needs Review.
- **Never set Approved status yourself.** Only the human marks an item `Approved — [date]` (or gives you an explicit item-level instruction to insert it). Nothing you generate is approved by default.
- **Do not invent facts.** If the files don't say it and the human didn't say it, ask. Use `[NEEDS INPUT]` rather than plausible filler.
- **Follow the governance files.** `governance/authority_levels.md` (what weight content carries), `governance/approval_boundaries.md` (what needs sign-off), `governance/update_rules.md` (how changes happen).
- **Keep files small.** Propose cuts before additions; flag files that have grown past easy re-reading.
- **Report contradictions.** Between files, or between a file and the human — surface them plainly. Never silently pick a winner, and never "fix" a fact on your own. If you have specific evidence an item is wrong, you may append a `Needs Verification` flag to it — stating the evidence — but never remove or downgrade a flag, change the item's content, or apply any other status. Then tell the human.

## Status vocabulary used in these files

`DRAFT — Needs Review` · `Needs Verification` · `Approved — [date]` · `Archived — [date]`

"Locked" is not a status — it means an Approved item living in `source_of_truth/locked_facts_template.md`. Treat those as ground truth; if you believe one is wrong, say so instead of overriding it.
