# Workflow: Starting a New AI Session

Use this every time you start a session that should be aligned with your framework. The goal is that the assistant loads the right files, in the right order, and proves it understood them before you start working.

## If your tool can read files

**1. Point the assistant at the folder** (open it as a workspace, attach it, or give the path — whatever your tool supports).

**2. Give it this instruction:**

> Read FIRST_USE_WITH_AI.md in this folder and follow it. You're in "Situation B" — loading an existing framework. Read the files in the order it specifies, then confirm your understanding as it instructs.

`FIRST_USE_WITH_AI.md` handles the rest: it sets the ground rules (proposals only, no self-approval, no time estimates) and specifies the read order — governance first, then core context, then source of truth, then decisions.

**3. Check the confirmation.** The assistant should play back its understanding of your current context and priorities in a few sentences. Read it. If it's wrong, correct it now — a session that starts misaligned stays misaligned. If the assistant reports missing files or contradictions, resolve those before working.

*Tip: if your tool auto-loads a `CLAUDE.md` or `AGENTS.md` instructions file, copy the matching file from `templates/` into place once — then step 2 happens automatically in every session. Note the split: Claude Code reads `CLAUDE.md` (not `AGENTS.md`); Codex, Cursor, and most other tools read `AGENTS.md`. If you use tools from both families, copy both files.*

## If your tool can only take pasted text

**1. Paste, in this order:** `FIRST_USE_WITH_AI.md`, then `governance/authority_levels.md`, `governance/approval_boundaries.md`, and `governance/update_rules.md`, then `core_context/operating_rules_template.md` and `do_not_do_template.md`, then `source_of_truth/locked_facts_template.md` and `current_priorities_template.md`, then `core_context/current_working_context_template.md`. Add `decisions/` files when the session involves drafting in your voice.

**2. If that's too much for your tool's limits, prioritize:** governance summaries can be compressed to one line each ("You may propose changes but never approve them; everything you draft is DRAFT — Needs Review"), but paste locked facts and current working context in full — those are the files where paraphrasing loses the exact wording that matters.

**3. Ask for the same confirmation** as above before starting work.

## During the session

- Anything the assistant drafts is a proposal until you review it — outputs included, not just file changes.
- If the session produces a change worth keeping, run `workflows/decision_review_workflow.md` before it enters a file.
- If the assistant contradicts a file, or two files contradict each other, it should tell you rather than pick a winner. If it doesn't, ask.

## Ending the session

One question, not a ritual: did anything change that future sessions should know? If yes — update `current_working_context`, or log the decision. If no, just close it.
