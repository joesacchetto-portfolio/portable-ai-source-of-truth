# Portable AI Source of Truth

A markdown-based starter kit for building your own portable "source of truth" folder — a small set of plain-text files that keep AI assistants aligned with your facts, preferences, and boundaries across tools and sessions.

## What this is

When you work with AI assistants on high-context work — managing projects, running implementations, consulting, coordinating teams — every new session starts from zero. You re-explain the same facts, the same constraints, the same "please don't do that" rules. Built-in memory features help, but they are tool-specific, hard to inspect, and not portable.

This kit takes a different, simpler approach: you keep your context in a folder of markdown files that you own, read, edit, and carry between tools. At the start of a session, you point the assistant at the folder. The files tell it what is true, what matters right now, what it may do on its own, and what requires your sign-off.

This is not a new idea. Developers have used files like `CLAUDE.md` and `AGENTS.md` for this purpose for a while, and the broader concepts here (context files, human-in-the-loop review, decision logs) are borrowed from existing practice. This kit adapts those ideas into a structure that non-technical users can copy and fill in without writing any code.

## What this is not

- **Not a memory engine or database.** It's a folder of text files. Nothing runs in the background, nothing syncs, nothing indexes.
- **Not a replacement for platform memory.** ChatGPT, Claude, and other tools have their own memory features. This kit works alongside them and gives you a portable, inspectable layer they don't provide.
- **Not an enterprise platform.** There is no server, no dashboard, no integration to install. If your organization needs governed AI infrastructure, this is not that.
- **Not autonomous.** Nothing an AI writes into these files is "true" until you have read it and approved it. Human review is the whole point.

## Who it's for

Project managers, implementation leads, operators, consultants, and solo users — anyone doing high-context work with AI assistants who wants consistency without building a technical system. No coding required. If you can edit a text file, you can use this.

Works with ChatGPT, Claude, Codex, Cursor, and any other assistant that can read files or accept pasted text.

## Repo map

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
| `core_context/operating_rules_template.md` | Your standing working preferences and constraints. |
| `core_context/do_not_do_template.md` | Explicit prohibitions the AI must respect. |
| `core_context/current_working_context_template.md` | Current-work "what I'm working on right now" file, updated when your active work changes. |
| `source_of_truth/locked_facts_template.md` | Human-approved facts the AI must treat as ground truth. |
| `source_of_truth/current_priorities_template.md` | Ranked list of what matters now. |
| `workflows/transcript_summary_workflow.md` | Steps for turning a transcript into approved context updates. |
| `workflows/decision_review_workflow.md` | Steps for reviewing an AI-proposed change before accepting it. |
| `workflows/agent_prompt_workflow.md` | How to start a new AI session so it loads the right files in the right order. |
| `decisions/decision_log_template.md` | Append-only record of decisions, with date, rationale, and status. |
| `decisions/approved_phrasing_template.md` | Wording you have approved for reuse in AI outputs. |
| `decisions/rejected_patterns_template.md` | Wording and behaviors you have rejected, so the AI stops repeating them. |
| `prompts/01_create_context_seed.md` | Prompt that interviews you to draft your initial context in one document. |
| `prompts/02_split_seed_into_files.md` | Prompt that splits the seed into the framework's files. |
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
