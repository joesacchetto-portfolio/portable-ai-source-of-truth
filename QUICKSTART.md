# Quickstart (for humans)

This guide gets you from an empty copy of this repo to a first working source-of-truth folder. No coding involved.

## What you'll end up with

A folder of short markdown files that describe your work context: what's true, what matters right now, what an AI may do on its own, and what needs your sign-off. You'll point AI assistants at this folder at the start of a session so they behave consistently.

## Before you start

- You need a plain-text editor — and you already have one. `.md` files are ordinary text: on Windows, Notepad opens them; on Mac, TextEdit does. Nothing to install. If double-clicking a `.md` file opens the wrong app (or nothing), right-click the file and choose **Open With** → Notepad or TextEdit. Mac TextEdit users: if you create a *new* file, use **Format → Make Plain Text** first, and turn off **Edit → Substitutions → Smart Quotes** so quotes aren't silently reformatted. (If you already have an editor you like — VS Code, Obsidian, Notepad++ — use that.)
- You need an AI assistant that can read files or accept pasted text (ChatGPT, Claude, Codex, Cursor, or similar).
- Decide where the folder will live: on your computer, in a synced drive, or in a private git repo. Anywhere you can find it again.

## Step 1 — Copy this repo

Download or clone this repository and rename the folder to something meaningful to you. This copy is yours; edit anything.

Never used GitHub before? No account or git needed: on the repository page, click the green **Code** button, choose **Download ZIP**, and unzip the downloaded file somewhere you can find it (your Documents folder works fine). To unzip: on Windows, right-click the file → **Extract All**; on Mac, just double-click it. The unzipped folder is your copy.

A note on how the fillable files work: the repo ships with blank templates under each folder's `starter/` subfolder (e.g. `decisions/starter/decision_log_template.md`). You never fill in or rename these yourself. When you run the setup prompts (prompt 02 in particular), the assistant automatically creates the live, cleanly-named file next to each starter folder (e.g. `decisions/decision_log.md`) with your content in it. The starter files stay blank as a permanent reference; the live files are what you and your assistants read and update day to day. If a live file doesn't exist yet under its plain name, that just means setup hasn't been completed — except `decisions/approved_phrasing.md` and `decisions/rejected_patterns.md`, which are never created during setup at all; they're created on first need (see `governance/update_rules.md`).

## Step 2 — Read two short files

Read `docs/privacy_and_review_warnings.md` first. It covers what should never go into these files. Then skim `README.md`'s repo map so you know what each file is for.

## Step 3 — Run the setup prompts with your AI assistant

The `prompts/` folder contains four numbered prompts. Use them in order, in a session with your AI assistant:

1. **`01_create_context_seed.md`** — the assistant interviews you and drafts a single "seed" document describing your context.
2. **`02_split_seed_into_files.md`** — the assistant splits the seed into the framework's live files, using the starter templates as the structure to follow.
3. **`03_review_and_activate.md`** — the assistant walks you through reviewing every generated file. You correct, cut, and approve.
4. **`04_audit_for_drift.md`** — save this one for after setup; run it periodically to catch contradictions and stale facts.

If your assistant can read files directly, also point it at `FIRST_USE_WITH_AI.md` — it contains the instructions the assistant should follow during setup.

A heads-up on effort: if your tool **cannot** read files (a plain chat window), prompt 02 involves pasting your seed document plus several blank starter templates into the session. It works, but it's the most tedious path — a tool that can read files directly (Claude, Cursor, ChatGPT with file upload, or similar) makes this step much easier.

Not sure what you're building toward? `examples/sample_project_manager_framework.md` shows what a completed (fictional) framework looks like — worth a skim before you start.

## Step 4 — Review everything

This step is not optional — though if you ran prompt 03 in Step 3, its guided review is where most of it happens. Prompt 03 walks you through approving each item; this step is your confirmation that it's done and nothing slipped through. Nothing the assistant wrote is "true" until you have read and approved it. Watch for:

- Facts the assistant guessed or embellished.
- Preferences stated more strongly than you actually hold them.
- Anything confidential that slipped in — remove it.

Mark files you've reviewed as approved (your live files carry the same `Status:` format most starter templates did — see any starter file for the example). Delete or fix anything wrong. Unreviewed content stays unapproved.

## Step 5 — Use it

At the start of a new AI session, follow `workflows/agent_prompt_workflow.md`: point the assistant at the folder (or paste the key files) and tell it to read `FIRST_USE_WITH_AI.md` first. If your tool supports `CLAUDE.md` or `AGENTS.md` instruction files, copy the ones in `templates/` into the folder where you work with your AI tool.

## Keeping it healthy

- Update `core_context/current_working_context.md` whenever your active work changes — it's meant to track your current state, not history. (If this file doesn't exist yet, setup hasn't been completed — see `core_context/starter/current_working_context_template.md` and prompt 02.)
- Log meaningful decisions in `decisions/decision_log.md` as they happen. (If this file doesn't exist yet, setup hasn't been completed — see `decisions/starter/decision_log_template.md` and prompt 02.)
- Run `prompts/04_audit_for_drift.md` periodically, on a schedule you choose.
- If a file has grown too long to willingly re-read, prune it. Small is the feature.

## If you get stuck

The example in `examples/sample_project_manager_framework.md` shows a completed (fictional) framework. When in doubt, write less than you think you need — you can always add more later.
