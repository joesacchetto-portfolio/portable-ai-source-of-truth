# Prompt 01 — Create Your Context Seed

**What this does:** Your AI assistant interviews you and drafts one "seed" document — a rough first pass at your whole context. Later prompts split it into the framework's files.

**Before you start:** Read `docs/privacy_and_review_warnings.md`. Don't share secrets, confidential material, or other people's private information during the interview.

**How to use:** Copy everything below the line into a new session with ChatGPT, Claude, Codex, Cursor, or a similar tool. Answer the questions one at a time.

---

I'm setting up a personal "source of truth" folder — a small set of markdown files that keep AI assistants aligned with my work context. Your job right now is to interview me and then draft a single seed document. Rules:

1. Ask me **one question at a time**. Wait for my answer before the next question.
2. Prefer concrete questions over broad ones. If my answer is vague, ask one follow-up, then move on.
3. **Do not invent anything.** If I haven't told you something, leave a `[NEEDS INPUT]` placeholder. Never fill gaps with plausible guesses.
4. If I mention passwords, confidential material, health details, or other people's private information, warn me and leave it out of the draft.
5. This interview covers my working context, not my life story. Keep it professional and practical.

Interview me on these areas, in order:

- **Role and work:** What I do, for whom, and what a typical week involves.
- **Current focus:** The 1–3 projects or goals that matter most right now, and roughly why.
- **Facts assistants get wrong:** The details about my work that AI assistants most often misstate, misremember, or assume incorrectly.
- **How I like to work:** Communication style, format preferences, level of detail, tools I use, how I want drafts delivered.
- **Hard "don'ts":** Things an assistant should never do, say, assume, or suggest when working with me.
- **What needs my sign-off:** Actions or outputs I always want to approve before they're final (e.g., anything sent to others, anything committing me to dates or money).
- **Recurring workflows:** Tasks I do repeatedly with AI help, worth standardizing.

When the interview is done, produce **one markdown document** titled "Context Seed" with a section per area above, using my words wherever possible. At the top, add:

> Status: DRAFT — Needs Review. Nothing in this document is approved until the human owner has read and confirmed it.

Do not mark anything as Approved — that's my job, not yours. End by telling me to (1) save the seed document somewhere I can find it, and (2) read the whole seed carefully and correct anything wrong, before moving to the next step (`prompts/02_split_seed_into_files.md`).
