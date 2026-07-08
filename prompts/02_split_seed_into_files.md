# Prompt 02 — Split the Seed into Files

**What this does:** Your AI assistant takes your reviewed Context Seed and sorts its content into the framework's files.

**Before you start:** Read `imports/context_seed.md` and fix anything wrong. Do not split a seed you have not read — errors multiply once they are spread across files. If the seed started as an AI-memory draft, review it especially carefully: remove sensitive material, correct unsupported claims, and mark uncertain items before continuing.

**Input:** the reviewed and corrected Context Seed from `imports/context_seed.md` only. If raw per-tool seed files also exist in `imports/`, they are source material for Prompt 01, not input for this split.

**Output:** the first set of live framework files in `core_context/`, `source_of_truth/`, and `decisions/`, plus any draft setup additions under `governance/approval_boundaries.md`'s "My additional sign-off items" section. Everything remains draft until Prompt 03 review.

**How to use:** Copy everything below the line into a session, along with your reviewed Context Seed (paste it or let the tool read `imports/context_seed.md`). If the tool can write files directly, it creates the live files for you. If it cannot write files, it outputs each file's content for you to paste into the live file paths listed below, not into the `starter/` templates.

If the assistant cannot read the repo files directly, paste your reviewed Context Seed plus these starter templates:

- `core_context/starter/operating_rules_template.md`
- `core_context/starter/do_not_do_template.md`
- `core_context/starter/current_working_context_template.md`
- `source_of_truth/starter/locked_facts_template.md`
- `source_of_truth/starter/current_priorities_template.md`
- `decisions/starter/decision_log_template.md`

You do not need to paste `approved_phrasing_template.md` or `rejected_patterns_template.md` during setup; those files are created later only if needed.

---

I have reviewed and corrected `imports/context_seed.md`. I also have a folder containing blank starter templates (each folder's `starter/` subfolder). Your job is to sort the seed's content into the right files. Rules:

1. **Sort, don't create.** Use only what's in the seed. Do not add new facts, preferences, or examples. If a template section has no matching seed content, write `[NEEDS INPUT]` and move on.
2. **Everything you produce enters as `DRAFT — Needs Review`**, placed the way each starter template already marks status — a file-level `Status:` line where the template has one, per-item status marks otherwise (locked facts and decision-log entries are per-item). Do not mark anything Approved. Only I can do that, in the next step.
3. If a piece of seed content could fit two files, put it in the more specific one and note the choice so I can review it.
4. If you spot likely secrets or private information about others in the seed, flag it and leave it out.
5. Keep each file short. Cut filler; keep my wording where you can.
6. Do not create `decisions/approved_phrasing.md` or `decisions/rejected_patterns.md` during this step, even if the seed contains content that seems to fit — those are created on first need during real use, not during setup (see `governance/update_rules.md`).
7. Do not treat `imports/context_seed.md` as governed context. It is source material for this split, not a live framework file. Do not split raw engine-specific seed files directly.

Sort the seed into these files. For each one: copy the structure/format from the blank starter template at `[folder]/starter/[name]_template.md`, then create the live file `[folder]/[name].md` with that structure filled in from the seed content. Never modify the starter file itself — it stays as the blank reference.

- `core_context/operating_rules.md` — my standing working preferences and constraints (from "How I like to work"). Structure from `core_context/starter/operating_rules_template.md`.
- `core_context/do_not_do.md` — explicit prohibitions (from "Hard don'ts"). Structure from `core_context/starter/do_not_do_template.md`.
- `core_context/current_working_context.md` — what I'm working on right now (from "Current focus" — the current-work detail). Structure from `core_context/starter/current_working_context_template.md`.
- `source_of_truth/locked_facts.md` — stable facts about my role and work (from "Role and work" and "Facts assistants get wrong"). These are *candidates* for locking — they still enter as DRAFT. Structure from `source_of_truth/starter/locked_facts_template.md`.
- `source_of_truth/current_priorities.md` — my ranked priorities (from "Current focus" — the durable ranking). Structure from `source_of_truth/starter/current_priorities_template.md`.
- `governance/approval_boundaries.md` — what needs my sign-off (from "What needs my sign-off") — add entries under the "My additional sign-off items" section only, replacing the "(none yet …)" placeholder line; do not alter any other part of that file. (This is a fixed governance file, not a starter template — edit it in place.)
- `decisions/decision_log.md` — leave mostly empty; add only decisions explicitly stated in the seed, dated today, marked DRAFT. Structure from `decisions/starter/decision_log_template.md`.

Anything in the seed about "Recurring workflows" should be listed at the end as **suggestions** for me to adapt into the `workflows/` files myself — don't write those files.

Follow the structure each starter template already has. When done, list every file you created, note any `[NEEDS INPUT]` gaps and judgment calls, and tell me the next step is reviewing everything with `prompts/03_review_and_activate.md`.