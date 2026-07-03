# Authority Levels

This file defines how much weight different kinds of context carry. When an AI assistant reads this folder, not everything in it deserves equal trust. These levels tell the assistant (and remind you) what to rely on, what to treat as tentative, and what to ignore.

## The levels

Listed from most to least authoritative:

### 1. Locked Facts

Human-approved facts the assistant must treat as ground truth. It must not contradict, "correct," or restate them differently. If the assistant believes a locked fact is wrong, it says so to the human — it never silently overrides one.

Lives mainly in: `source_of_truth/locked_facts_template.md`

### 2. Strong Preferences

Standing rules about how the human works and what the assistant must or must not do. The assistant follows these by default in every session. Deviating requires asking first.

Lives mainly in: `core_context/operating_rules_template.md`, `core_context/do_not_do_template.md`, `decisions/approved_phrasing_template.md`, `decisions/rejected_patterns_template.md`

### 3. Working Assumptions

Current context and priorities that are believed true right now but expected to change. The assistant uses these to guide its help, and states the assumption when output depends on one ("Assuming X is still your top priority…").

Lives mainly in: `core_context/current_working_context_template.md`, `source_of_truth/current_priorities_template.md`

### 4. Needs Verification

Items flagged as uncertain, stale-looking, or not yet confirmed — including anything still marked DRAFT — Needs Review. The assistant may mention these but must not rely on them without saying so, and must not repeat them as fact.

Can appear in any file, marked with its status.

### 5. Archived

Material kept for history: superseded facts, closed projects, old decisions. The assistant ignores archived material unless the human asks about it directly. Archived content never overrides anything above it.

Lives mainly in: dated "Archive" sections at the bottom of files, or entries marked Archived in the decision log.

## How conflicts resolve

A higher level always beats a lower one. If two items at the **same** level conflict, the assistant does not pick a winner — it reports both to the human and asks. If a file's content conflicts with what the human says in the current session, the human wins, and the assistant should offer to update the file (following `update_rules.md`).

## Moving between levels

Content only moves **up** a level (toward Locked) through explicit human approval — see `update_rules.md`. An AI assistant may propose a promotion; it may never perform one on its own. Moving **down** (e.g., a locked fact becoming stale and getting archived) also requires the human's say-so, with one exception: an assistant may append a `Needs Verification` flag (with specific stated evidence) to any item, which suspends that item's authority until the human resolves it. Assistants never remove flags, archive content, or demote anything further on their own.
