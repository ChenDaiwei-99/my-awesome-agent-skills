---
name: kb-schema
description: Create and evolve human-friendly Obsidian workspace schemas with an assistant-maintained LLM knowledge base and a human-owned personal note space. Use when setting up or changing AGENTS.md, knowledge-base raw/wiki folders, fleeting/projects/permanent note folders, project note templates, or ownership rules that prevent agents from overwriting the user's own notes.
---

# KB Schema

Use this skill to define the operating contract for an Obsidian-backed workspace. The goal is a vault with two clear spaces: an assistant-maintained LLM wiki for external knowledge, and a human-owned personal note space for fleeting thoughts, project work, and durable personal principles.

## Core Principles

- Keep personal notes human-owned. Link/frontmatter formatting changes may be applied directly; before substantive content changes under `personal-notes/`, list the exact proposed file changes and wait for the user's approval.
- Keep the knowledge base agent-maintained. Agents may update `knowledge-base/raw/` and `knowledge-base/wiki/` according to the local `AGENTS.md`.
- Preserve all source links. A future agent should be able to retrieve deeper details from the internet when the local raw-source record is insufficient.
- Use conservative conflict handling. Do not silently overwrite contested claims; route contradictions to `knowledge-base/wiki/review.md`.
- Prefer simple folders and lightweight frontmatter over systems that make manual writing tedious.

## Workflow

1. Read the vault root `AGENTS.md` if it exists. Treat it as the project-specific override.
2. Inspect top-level folders before proposing changes. Preserve existing user conventions unless they conflict with the human/source/wiki ownership split.
3. Create or update the standard workspace layout from [layout.md](references/layout.md).
4. Define personal note conventions from [human-notes.md](references/human-notes.md).
5. Define raw-source record conventions from [source-records.md](references/source-records.md).
6. Seed missing control files: `knowledge-base/wiki/index.md`, `knowledge-base/wiki/log.md`, `knowledge-base/wiki/review.md`, and `knowledge-base/wiki/note-advice/`.
7. Update `AGENTS.md` with the final schema, ownership rules, citation rules, and conflict policy.
8. Validate that folder names, frontmatter fields, and required wiki files match the chosen schema.

## AGENTS.md Requirements

Include these sections in the vault root `AGENTS.md`:

- Knowledge base purpose and audience.
- Folder ownership rules for `knowledge-base/` and `personal-notes/`.
- Personal note schema and optional templates.
- Raw-source record schema for PDF, GitHub, web, and other sources.
- Citation and preserved-link policy.
- Conflict policy and review queue format.
- Index, log, and advisory report maintenance rules.

## References

- [layout.md](references/layout.md): standard folder layout and ownership matrix.
- [human-notes.md](references/human-notes.md): easy-to-maintain human note schema.
- [source-records.md](references/source-records.md): one-file-per-raw-source record templates.
