# Prompt 04 — Audit for Drift

**What this does:** Your AI assistant checks your framework for staleness, contradictions, bloat, and privacy risks, and hands you a short punch list. Run it periodically, on a schedule you choose, or after any big change in your work.

**What it doesn't do:** Fix things on its own. The audit proposes; you decide.

**How to use:** Copy everything below the line into a session where the assistant has access to your framework files (or paste them in).

---

Audit my source-of-truth folder for drift. Read all the files, then report. **During the audit phase do not modify, create, delete, rename, or move any file, and do not fix anything you find — report only.** Edits happen later, one item at a time, only after I approve a specific change. Check for:

1. **Stale content.** Approved items that look outdated: past-tense deadlines, finished projects still listed as active, a `current_working_context` that hasn't changed in a while. Flag each with why it looks stale.
2. **Contradictions.** Places where two files disagree — a locked fact vs. current context, a priority vs. an operating rule, a rejected pattern that still appears elsewhere. Quote both sides.
3. **Status hygiene.** Items still marked DRAFT or Needs Verification that I may have forgotten, and any item that somehow lacks a status. Also flag anything marked Approved that has clearly been edited since (if you can tell).
4. **Bloat.** Files that have grown past the point I'd willingly re-read. Suggest specific cuts or items to archive — the framework only works if it stays short.
5. **Privacy risks.** Anything that looks like credentials, confidential material, or other people's private information. Flag these first and separately.
6. **Drift from reality.** Ask me up to five short questions to test whether key approved items still match my actual situation (e.g., "Is X still your top priority?"). Base the questions on what you read.

Then give me a punch list, ordered: privacy risks first, contradictions second, everything else after. For each item: the file, the problem, and a proposed fix.

Walk me through the list one item at a time and let me accept, edit, or skip each fix. Rules for applying fixes:

- Only apply a fix after I explicitly accept it.
- Any new or changed content enters as `DRAFT — Needs Review` — an audit is not an approval. Only items I explicitly re-confirm keep or get `Approved` status.
- Never mark anything Approved on your own.

End with a two-line summary: what changed, and what I still owe (unresolved flags, unanswered gaps).
