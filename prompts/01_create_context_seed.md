# Prompt 01 — Create Your Context Seed

**What this does:** Your AI assistant helps you create one "Context Seed" document: a rough first pass at your work context. If you already have an AI assistant with useful memory or prior chat history, start by using that context as draft input. If not, the assistant interviews you from scratch. Later prompts split the reviewed seed into the framework's files.

**Before you start:** Read `docs/privacy_and_review_warnings.md`. Do not share secrets, confidential material, health information, or private details about other people. If you use an AI-generated rough seed, treat it as unreviewed draft material, not as fact.

**Output:** Prompt 01 produces one intermediate draft file: `imports/context_seed.md`. It does not create the live framework files. Prompt 02 does that after you review and correct the seed.

**How to use:** Use the optional first-step prompt below only if you already have an AI assistant with useful memory or prior context. Then copy the main setup prompt into the assistant that will help you create this framework.

## Optional first step — pull a rough seed from an AI that already knows you

If you already use an AI assistant with memory, long chat history, or prior context, run this prompt there first:

> I am setting up a portable AI source-of-truth folder. Draft a rough Context Seed from what you know about my work, preferences, recurring workflows, boundaries, and common corrections I have made. Do not include secrets, credentials, health information, confidential material, or private details about other people. Mark uncertain items as `[NEEDS VERIFICATION]`. Do not present anything as approved fact. This is only a rough draft for me to review.

Read the rough seed before using it. Delete anything sensitive or wrong. Then paste it into the setup session using the main prompt below.

If you do not have existing AI memory or prior context to use, skip this step and start from scratch with the main prompt.

---

I'm setting up a personal "source of truth" folder: a small set of markdown files that keep AI assistants aligned with my work context. Your job right now is to help me create a single Context Seed document.

If I provide a rough Context Seed, audit it first. Identify unsupported claims, privacy risks, contradictions, and gaps. Then ask me one question at a time to confirm, correct, or fill the missing pieces.

If I do not provide a rough Context Seed, interview me from scratch.

Rules:

1. Ask me **one question at a time**. Wait for my answer before the next question.
2. Prefer concrete questions over broad ones. If my answer is vague, ask one follow-up, then move on.
3. **Do not invent anything.** If I have not confirmed something, leave a `[NEEDS INPUT]` placeholder or mark it `[NEEDS VERIFICATION]`. Never fill gaps with plausible guesses.
4. Do not treat an AI-generated rough seed as true just because another assistant produced it. It is draft input only.
5. If I mention passwords, confidential material, health details, or other people's private information, warn me and leave it out of the draft.
6. This process covers my working context, not my life story. Keep it professional and practical.
7. Do not create or edit the live framework files during this prompt. Only produce the Context Seed.

Cover these areas, in order. If a rough seed already covers an area, verify it and ask only what is needed to correct or complete it:

- **Role and work:** What I do, for whom, and what a typical week involves.
- **Current focus:** The 1-3 projects or goals that matter most right now, and roughly why.
- **Facts assistants get wrong:** The details about my work that AI assistants most often misstate, misremember, or assume incorrectly.
- **How I like to work:** Communication style, format preferences, level of detail, tools I use, how I want drafts delivered.
- **Hard "don'ts":** Things an assistant should never do, say, assume, or suggest when working with me.
- **What needs my sign-off:** Actions or outputs I always want to approve before they are final, such as anything sent to others or anything committing me to dates or money.
- **Recurring workflows:** Tasks I do repeatedly with AI help, worth standardizing.

When the verification and gap-filling are done, produce **one markdown document** titled "Context Seed" with a section per area above, using my words wherever possible. At the top, add:

> Status: DRAFT — Needs Review. Nothing in this document is approved until the human owner has read and confirmed it.

If you can write files, save the document as `imports/context_seed.md`. If you cannot write files, return the complete markdown document and tell me to save it as `imports/context_seed.md`.

Do not mark anything as Approved. That is my job, not yours. End by telling me to (1) read `imports/context_seed.md` carefully, (2) correct anything wrong or sensitive, and (3) use the reviewed seed as the input to `prompts/02_split_seed_into_files.md`.