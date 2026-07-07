# Imports

This folder is for setup input brought into the framework before it becomes governed source-of-truth content.

During setup, Prompt 01 should save the final draft seed here:

```text
imports/context_seed.md
```

If you use multiple AI assistants to create rough seeds, save each raw seed separately before merging, for example:

```text
imports/context_seed_chatgpt.md
imports/context_seed_claude.md
imports/context_seed_gemini.md
imports/context_seed_other.md
```

`imports/context_seed.md` is the single reviewed draft seed used by `prompts/02_split_seed_into_files.md`. The engine-specific files are raw imports only. Agreement across tools is not proof, and contradictions should be flagged for human review.

Nothing in `imports/` is approved source-of-truth content. These files may include AI-memory output, rough notes, mistakes, stale context, or sensitive details that should be removed. Read and correct the merged seed before running `prompts/02_split_seed_into_files.md`.

After setup, you can keep these files as historical source material, move them elsewhere, or delete them if you do not want unreviewed draft context stored in the folder.
