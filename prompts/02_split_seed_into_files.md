# Prompt 02 — Split the Seed into Files

**What this does:** Your AI assistant takes your reviewed Context Seed and sorts its content into the framework's files.

**Before you start:** Read your seed document and fix anything wrong. Don't split a seed you haven't read — errors multiply once they're spread across files.

**How to use:** Copy everything below the line into a session, along with your Context Seed (paste it or let the tool read the file). If the tool can write files directly, it can fill in the templates; otherwise it outputs each file's content for you to paste in yourself. If the assistant cannot read the repo files directly, paste the Context Seed and the relevant template files, or paste the template structure you want it to follow.

---

I have a "Context Seed" document (provided) and a folder of template files. Your job is to sort the seed's content into the right files. Rules:

1. **Sort, don't create.** Use only what's in the seed. Do not add new facts, preferences, or examples. If a template section has no matching seed content, write `[NEEDS INPUT]` and move on.
2. **Every file you produce starts with:** `Status: DRAFT — Needs Review`. Do not mark anything Approved. Only I can do that, in the next step.
3. If a piece of seed content could fit two files, put it in the more specific one and note the choice so I can review it.
4. If you spot likely secrets or private information about others in the seed, flag it and leave it out.
5. Keep each file short. Cut filler; keep my wording where you can.

Sort the seed into these files:

- `core_context/operating_rules_template.md` — my standing working preferences and constraints (from "How I like to work").
- `core_context/do_not_do_template.md` — explicit prohibitions (from "Hard don'ts").
- `core_context/current_working_context_template.md` — what I'm working on right now (from "Current focus" — the current-work detail).
- `source_of_truth/locked_facts_template.md` — stable facts about my role and work (from "Role and work" and "Facts assistants get wrong"). These are *candidates* for locking — they still enter as DRAFT.
- `source_of_truth/current_priorities_template.md` — my ranked priorities (from "Current focus" — the durable ranking).
- `governance/approval_boundaries.md` — what needs my sign-off (from "What needs my sign-off").
- `decisions/decision_log_template.md` — leave mostly empty; add only decisions explicitly stated in the seed, dated today, marked DRAFT.

Anything in the seed about "Recurring workflows" should be listed at the end as **suggestions** for me to adapt into the `workflows/` files myself — don't write those files.

Follow the structure each template already has. When done, list every file you filled in, note any `[NEEDS INPUT]` gaps and judgment calls, and tell me the next step is reviewing everything with `prompts/03_review_and_activate.md`.
