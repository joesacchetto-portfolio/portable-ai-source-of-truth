# Prompt 03 — Review and Activate

**What this does:** Your AI assistant walks you through every drafted file, item by item, so you can approve, fix, or cut each one. This is the step that turns drafts into your actual source of truth.

**Do not skip this.** Unreviewed files will confidently mislead every future session. The value of the whole framework is created here.

**How to use:** Copy everything below the line into a session where the assistant has access to your drafted files (or paste the files in).

---

I have a folder of DRAFT files created from my context seed. Walk me through reviewing them. Rules:

1. **Go file by file, and within each file, item by item.** For each item, show it to me and ask: keep as-is, edit, or delete? One item at a time.
2. **You never approve anything.** When I confirm an item, you update it per my instruction — but only I decide. If I say "just approve everything without showing me," push back once: unread approvals defeat the purpose of the framework. If I still insist, leave everything marked DRAFT and tell me why.
3. For each item, help me pressure-test it briefly:
   - Is it actually true, or did the drafting step round it into a cleaner story?
   - Is a preference stated more strongly than I really hold it?
   - Would I be comfortable with this being sent to an AI provider in every future session?
   - Is it about another person in a way that isn't mine to record?
4. Anything I confirm: change its status to `Approved — YYYY-MM-DD` (today's date). Anything I'm unsure about: mark `Needs Verification`. Anything cut: delete it, don't comment it out. This confirmation is my explicit item-level instruction to insert that status, per governance/update_rules.md.
5. For `source_of_truth/locked_facts_template.md`, be extra strict — these will be treated as ground truth. Only facts I explicitly confirm, one by one, get `Approved`. Suggest moving anything time-sensitive to `current_working_context` instead.
6. Keep a running list of `[NEEDS INPUT]` gaps we hit; at the end, ask me whether to fill them now or leave them.

Review the files in this order: `governance/` (all three), `core_context/` (all three), `source_of_truth/` (both), `decisions/` (all three), then anything else that's in DRAFT.

When we finish, give me a short closing summary: which files are fully Approved, which contain Needs Verification items, and which still have gaps. Remind me that the framework is now live, that I should update `current_working_context` when my active work changes, and that I should run `prompts/04_audit_for_drift.md` periodically.
