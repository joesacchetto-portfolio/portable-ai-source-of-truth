# Portable AI Source of Truth

A plain-text starter kit for everyday AI users who want assistants to stay aligned with the right facts, preferences, priorities, and boundaries across tools and sessions — without adopting a database, app, or developer workflow.

Full case study — background, design decisions, and findings: [joesacchetto.com/portable-ai-source-of-truth](https://joesacchetto.com/portable-ai-source-of-truth)

## What this is

When you work with AI assistants on high-context work — managing projects, running implementations, consulting, coordinating teams — every new session starts from zero. You re-explain the same facts, the same constraints, the same "please don't do that" rules. Built-in memory features help, but they are tool-specific, hard to inspect, and not portable.

Developers, engineers, AI builders, and power users already have ways to manage this problem through project instructions, coding-agent rules, decision logs, and local documentation. Those patterns are useful, but they are often shaped by developer environments.

This kit adapts that discipline into a smaller plain-text folder for recurring high-context work in delivery, operations, consulting, and project settings.

This kit takes a different, simpler approach: you keep your context in a folder of markdown files that you own, read, edit, and carry between tools. At the start of a session, you point the assistant at the folder. The files tell it what is true, what matters right now, what it may do on its own, and what requires your sign-off.

That means you can start work in one AI tool, close it, then continue in another tool by pointing the new assistant at the same folder. For example: start in Codex, continue in Claude, then later use ChatGPT with the same source-of-truth folder.

## What this is not

- **Not a memory engine or database.** It's a folder of text files. Nothing runs in the background, nothing syncs, nothing indexes.
- **Not a replacement for platform memory.** ChatGPT, Claude, and other tools have their own memory features. This kit works alongside them and gives you a portable, inspectable layer they don't provide.
- **Not an enterprise platform.** There is no server, no dashboard, no integration to install. If your organization needs governed AI infrastructure, this is not that.
- **Not autonomous.** Nothing an AI writes into these files is "true" until you have read it and approved it. Human review is the whole point.

## Who it's for

This is for people doing recurring high-context work — project managers, operators, consultants, founders, analysts, recruiters, account managers, customer success leads, coordinators, executive assistants, and solo users — who need AI assistants to stay consistent without learning engineering-style tooling. No coding required. If you can edit a text file, you can use this.

This is not a new idea. Developers have used files like `CLAUDE.md` and `AGENTS.md` for this purpose for a while, and the broader concepts here — context files, human review, decision logs, and local documentation — are borrowed from existing practice. This kit adapts those ideas into a smaller plain-text structure that everyday AI users can copy, review, and maintain without writing code.

Works with ChatGPT, Claude, Codex, Cursor, and any other assistant that can read files or accept pasted text.

## Best way to use it

This framework is easiest to use with an AI assistant that can read a local folder. In that setup, you point the assistant at this downloaded folder, then ask it to follow `QUICKSTART.md` or `FIRST_USE_WITH_AI.md`. The assistant can read the starter files, create the missing live files, and tell you what to review.

Examples include coding assistants and desktop tools that can open or connect to a local project folder. If your AI tool only works through a web chat, you can still use this framework, but you may need to upload files, paste file contents, or copy the assistant's proposed changes back into the folder yourself.

If you are not sure whether your AI tool can read a folder, ask it:

```text
Can you read or work with a local folder on my computer if I point you to it? If yes, tell me how to connect you to this folder. If no, tell me the easiest way to use these markdown files with you through uploads, attachments, or copy and paste.
```

## Repo map

Fillable files follow a two-part pattern, shown below as *ships as → becomes*: the repo ships a blank template under a `starter/` subfolder, and setup (prompt 02) creates the live, cleanly-named file next to it. The live file is what you and your assistants use day to day; it doesn't exist until you've run setup. (Two exceptions: `decisions/approved_phrasing.md` and `decisions/rejected_patterns.md` are never created during setup — they're created on first need; see `governance/update_rules.md`.)

| Path | Purpose |
|---|---|
| `README.md` | This file: purpose, audience, map, and boundaries. |
| `QUICKSTART.md` | Human entry point — how to set up your own copy, step by step. |
| `FIRST_USE_WITH_AI.md` | AI entry point — instructions an assistant follows when helping you set up or when loading the framework in a new session. |
| `LICENSE` | MIT license. Copy and adapt freely. |
| `templates/AGENTS.md` | Drop-in instructions file for tools that read `AGENTS.md` conventions. |
| `templates/CLAUDE.md` | Drop-in instructions file for Claude-based tools. |
| `governance/authority_levels.md` | How much weight different types of context carry: locked facts, strong preferences, working assumptions, needs-verification items, archived material. |
| `governance/approval_boundaries.md` | Which actions, file changes, or external outputs require explicit human sign-off. |
| `governance/update_rules.md` | How, when, and by whom any file in the folder gets updated. |
| `imports/README.md` | Notes on setup input, including the draft `imports/context_seed.md` file created by Prompt 01. |
| `core_context/starter/operating_rules_template.md` → `core_context/operating_rules.md` | Your standing working preferences and constraints. |
| `core_context/starter/do_not_do_template.md` → `core_context/do_not_do.md` | Explicit prohibitions the AI must respect. |
| `core_context/starter/current_working_context_template.md` → `core_context/current_working_context.md` | Current-work "what I'm working on right now" file, updated when your active work changes. |
| `source_of_truth/starter/locked_facts_template.md` → `source_of_truth/locked_facts.md` | Human-approved facts the AI must treat as ground truth. |
| `source_of_truth/starter/current_priorities_template.md` → `source_of_truth/current_priorities.md` | Ranked list of what matters now. |
| `workflows/transcript_summary_workflow.md` | Steps for turning a transcript into approved context updates. |
| `workflows/decision_review_workflow.md` | Steps for reviewing an AI-proposed change before accepting it. |
| `workflows/agent_prompt_workflow.md` | How to start a new AI session so it loads the right files in the right order. |
| `decisions/starter/decision_log_template.md` → `decisions/decision_log.md` | Append-only record of decisions, with date, rationale, and status. |
| `decisions/starter/approved_phrasing_template.md` → `decisions/approved_phrasing.md` | Wording you have approved for reuse in AI outputs. |
| `decisions/starter/rejected_patterns_template.md` → `decisions/rejected_patterns.md` | Wording and behaviors you have rejected, so the AI stops repeating them. |
| `prompts/01_create_context_seed.md` | Prompt that helps you create the draft `imports/context_seed.md`, either from an existing AI-generated rough seed or from a guided interview. |
| `prompts/02_split_seed_into_files.md` | Prompt that splits the seed into the framework's live files. |
| `prompts/03_review_and_activate.md` | Prompt that walks you through reviewing and approving the split files. |
| `prompts/04_audit_for_drift.md` | Prompt that periodically checks files for contradictions and staleness. |
| `examples/sample_project_manager_framework.md` | One condensed, fully fictional example of a completed framework. |
| `docs/why_this_exists.md` | The problem, the prior art this adapts, and what the kit doesn't do. |
| `docs/privacy_and_review_warnings.md` | What not to store in plain text, and why human review is mandatory. |

## Safe-use boundaries

1. **Review before you trust.** Anything an AI drafts into these files is a proposal, not a fact, until you have read and approved it. Treat unreviewed content as unapproved.
2. **Plain text is not private.** Don't put passwords, API keys, health details, other people's personal information, or anything confidential into these files. Assume anything in the folder may be sent to an AI provider when you share it in a session. See `docs/privacy_and_review_warnings.md`.
3. **You are the source of truth.** The files record your decisions; they don't make them. If a file and your judgment disagree, fix the file.
4. **Keep it small.** The framework works because it's short enough to actually read. If a file grows past what you'd willingly re-read, prune or archive it.

## Getting started

Humans: start with `QUICKSTART.md`.
If you're an AI assistant reading this: go to `FIRST_USE_WITH_AI.md`.
