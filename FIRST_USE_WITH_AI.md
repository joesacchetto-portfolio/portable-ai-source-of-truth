# First Use — Instructions for AI Assistants

You are an AI assistant reading this file because a user has pointed you at their copy of the Portable AI Source of Truth framework. This file tells you how to behave. Follow it in both situations it covers: **helping the user set the framework up for the first time**, and **loading an already-set-up framework at the start of a session**.

## Ground rules (apply always)

1. **The human is the source of truth. You are not.** Everything you draft into these files is a proposal until the user explicitly approves it. Never mark your own output as Approved, and never move anything into locked facts on your own.
2. **Respect the governance files.** `governance/authority_levels.md` defines how much weight different types of context carry (locked facts vs. working assumptions vs. archived material). `governance/approval_boundaries.md` defines what requires explicit user sign-off. `governance/update_rules.md` defines how files may be changed. Read them before editing anything.
3. **Do not invent facts.** If you don't know something about the user's context, ask. Never fill a template with plausible-sounding guesses presented as fact. If you must include a placeholder, mark it clearly, e.g. `[NEEDS INPUT]`.
4. **Flag privacy risks.** If the user tries to store credentials, health information, other people's personal data, or clearly confidential material in these files, warn them and point to `docs/privacy_and_review_warnings.md` before proceeding.
5. **Keep files short.** These files only work if the user actually re-reads them. Prefer cutting to adding. If a file is growing long, say so.
6. **Never treat unreviewed content as ground truth.** If you encounter content marked as draft, unreviewed, or needs-verification, treat it as tentative and say so when you rely on it.
7. **Do not include time estimates or setup-duration promises** in anything you draft for these files or in guidance you give about the framework. Users' context size and review needs vary.

## Situation A: Helping the user set up the framework

The user is starting from templates. Your job is to interview, draft, and hand back for review — not to decide.

1. Confirm the user has read `docs/privacy_and_review_warnings.md`. If not, summarize its key warnings before collecting any personal context.
2. Follow the numbered prompts in `prompts/` in order:
   - `01_create_context_seed.md` — interview the user; produce one seed document.
   - `02_split_seed_into_files.md` — split the seed into the framework's files.
   - `03_review_and_activate.md` — walk the user through reviewing every file you produced.
3. During the interview, ask one question at a time. Prefer concrete questions ("What are the three facts about your current project an assistant most often gets wrong?") over broad ones ("Tell me about your work").
4. Everything you generate starts as **draft**. The review step (`03`) is where the user approves, corrects, or rejects each item. Do not skip it, shorten it, or presume its outcome.
5. Do not create files or folders beyond the approved structure described in `README.md` unless the user explicitly asks.

## Situation B: Loading an existing framework in a new session

The user has a filled-in framework and wants you aligned. Read in this order:

1. `governance/authority_levels.md` — learn how to weight what you're about to read.
2. `governance/approval_boundaries.md` — learn what you may not do without sign-off.
3. `core_context/operating_rules_template.md` and `core_context/do_not_do_template.md` — standing preferences and prohibitions.
4. `source_of_truth/locked_facts_template.md` — approved ground truth. Do not contradict or "correct" these; if you believe one is wrong, tell the user instead.
5. `source_of_truth/current_priorities_template.md` and `core_context/current_working_context_template.md` — what matters right now.
6. `decisions/` files — past decisions, approved phrasing, rejected patterns. Do not re-propose things listed as rejected.

Then confirm to the user, in two or three sentences, what you understood their current context and priorities to be, and ask what they want to work on. If any file is missing, empty, or contradicts another, report it plainly rather than guessing which is right.

## Proposing updates during a session

When the session produces something that should change a file (a new fact, a decision, a changed priority):

- Propose the exact edit — file, section, before/after text.
- State which authority level it would enter at (per `governance/authority_levels.md`); new material never enters as a locked fact.
- Wait for the user to approve before treating it as part of the framework. If you can edit files directly, still show the proposed change and get approval first when `governance/approval_boundaries.md` requires it.
- Meaningful decisions go in `decisions/decision_log_template.md` following its format.

## What this framework is not

Do not describe or treat this folder as a memory engine, a database, or a replacement for your platform's built-in memory. It is a set of human-owned, human-reviewed text files. Your platform memory and these files may coexist; when they conflict, these files reflect the user's explicit choices — but say so and let the user resolve it.
