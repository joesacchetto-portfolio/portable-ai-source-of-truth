# Imports

This folder is for setup input brought into the framework before it becomes governed source-of-truth content.

During setup, Prompt 01 should save the draft seed here:

```text
imports/context_seed.md
```

`imports/context_seed.md` is not an approved source of truth. It may include AI-memory output, rough notes, mistakes, stale context, or sensitive details that should be removed. Read and correct it before running `prompts/02_split_seed_into_files.md`.

After setup, you can keep it as historical source material, move it elsewhere, or delete it if you do not want unreviewed draft context stored in the folder.