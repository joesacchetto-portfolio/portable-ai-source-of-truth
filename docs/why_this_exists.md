# Why This Exists

## The problem

If you do high-context work with AI assistants — coordinating projects, running implementations, advising clients, operating anything with many moving parts — you've likely hit some version of these:

- **Drift.** Session ten describes your work differently than session one did, and neither quite matches reality.
- **Invented continuity.** The assistant "remembers" connections between things that were never connected, or confidently continues a plan you abandoned.
- **Stale assumptions.** A priority you dropped in the spring still shapes the suggestions you get in the fall.
- **Ignored boundaries.** Drafts get worded as commitments; things you never wanted raised keep coming back; the assistant decides things that were yours to decide.
- **Drafts treated as facts.** Something the assistant guessed in one session gets repeated in the next as if you'd confirmed it.

None of these are exotic failures. They're what happens by default when a probabilistic assistant works across many sessions with no stable, human-controlled record of what's true, what matters, and what it's allowed to do.

Platform memory features help with recall, but they don't solve governance: you can't easily see everything they hold, edit it line by line, carry it between tools, or control what authority a remembered item carries.

## What this kit does about it

It gives you a small folder of markdown files — readable by you, readable by assistants — that acts as the governed record an assistant checks against:

- **Reviewable source files.** Everything an assistant should treat as true or binding lives in plain text you can read and edit. No hidden state.
- **Authority levels.** Not everything carries equal weight. A locked fact, a preference, a working assumption, and a note that has not been checked are explicitly different things, and assistants are told to treat them differently.
- **Approval boundaries.** What an assistant may draft freely, what it must propose first, and what only you can do (like marking anything Approved) is written down, not assumed.
- **Repeatable workflows.** The error-prone moments — summarizing a transcript, accepting a proposed change, starting a fresh session — get short checklists instead of improvisation.
- **A review loop.** Everything AI-generated enters as a draft. It becomes part of your source of truth only after you've read that specific item and approved it. Drift gets caught by a periodic audit rather than accumulating silently.

The through-line: the human stays the source of truth. The files just make that enforceable.

## What this adapts (prior art)

Almost nothing here is original, and that's deliberate. This kit adapts practices that already work elsewhere:

- **Context and project instruction files** — developers have long used files like `CLAUDE.md` and `AGENTS.md` to keep coding assistants aligned with a project. This kit generalizes that pattern beyond code.
- **Human-in-the-loop review** — the draft → review → approve cycle is standard practice anywhere machine output has consequences.
- **Decision logs** — adapted from engineering decision records: write down what was decided and why, so it doesn't get relitigated.
- **Approval boundaries and authority levels** — simplified from how organizations handle delegation and sign-off generally.
- **Plain-text, file-based knowledge** — from the long tradition of markdown notes and docs-as-files: human-readable, portable, diffable, tool-neutral.

The contribution, such as it is, is packaging: these practices arranged into one small, copyable folder that a non-technical person can use without building anything.

## What this is not

- **Not a memory engine or database.** Nothing runs, syncs, or indexes. It's text files you edit.
- **Not a replacement for platform memory.** Use both. This is the portable, inspectable, governed layer; platform memory is convenience recall. When they conflict, these files record your explicit choices.
- **Not an autonomous agent system.** Nothing here grants an assistant authority to act alone. Most of the kit exists to do the opposite.
- **Not an enterprise platform.** No server, no dashboard, no admin console. If you need organizational AI governance with access controls and audit trails, this is a folder of markdown files and you need something else.
- **Not a guarantee.** Assistants can ignore instructions, and files can't force compliance. The kit reduces drift and catches errors at review time; it doesn't make an assistant trustworthy. Your review is the actual safety mechanism.

## Who it's for

PMs, implementation leads, operators, consultants, solo users — anyone doing high-context, AI-assisted work who needs consistency across sessions and tools without building or maintaining a technical system. If you can edit a text file and are willing to actually read what you approve, the kit works. If you're not willing to review, it won't — and that's a fair reason not to use it.
