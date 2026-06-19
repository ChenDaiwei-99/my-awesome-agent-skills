---
name: kb-schema
description: Create and evolve human-friendly Obsidian LLM knowledge-base schemas, AGENTS.md instructions, note/source/wiki folder conventions, and ownership rules. Use when setting up a knowledge base, changing its file layout, designing templates for human notes or source records, or making sure agents can maintain a KB without overwriting the user's own notes.
---

# KB Schema

Use this skill to define the operating contract for an Obsidian-backed knowledge base. The goal is a vault that stays comfortable for humans to write in while agents maintain source records, synthesis pages, indexes, logs, and review queues.

## Core Principles

- Keep human notes human-owned. Suggest edits, but do not rewrite `notes/` without explicit user permission.
- Keep source records and wiki synthesis agent-maintained. Agents may update `sources/` and `wiki/` according to the local `AGENTS.md`.
- Preserve all source links. A future agent should be able to retrieve deeper details from the internet when the local source record is insufficient.
- Use conservative conflict handling. Do not silently overwrite contested claims; route contradictions to `wiki/review.md`.
- Prefer simple folders and lightweight frontmatter over systems that make manual writing tedious.

## Workflow

1. Read the vault root `AGENTS.md` if it exists. Treat it as the project-specific override.
2. Inspect top-level folders before proposing changes. Preserve existing user conventions unless they conflict with the human/source/wiki ownership split.
3. Create or update the standard layout from [layout.md](references/layout.md).
4. Define human note conventions from [human-notes.md](references/human-notes.md).
5. Define source record conventions from [source-records.md](references/source-records.md).
6. Seed missing control files: `wiki/index.md`, `wiki/log.md`, `wiki/review.md`, and `wiki/note-advice/`.
7. Update `AGENTS.md` with the final schema, ownership rules, citation rules, and conflict policy.
8. Validate that folder names, frontmatter fields, and required wiki files match the chosen schema.

## AGENTS.md Requirements

Include these sections in the vault root `AGENTS.md`:

- Knowledge base purpose and audience.
- Folder ownership rules for `notes/`, `sources/`, and `wiki/`.
- Human note schema and optional templates.
- Source record schema for PDF, GitHub, web, and other sources.
- Citation and preserved-link policy.
- Conflict policy and review queue format.
- Index, log, and advisory report maintenance rules.

## References

- [layout.md](references/layout.md): standard folder layout and ownership matrix.
- [human-notes.md](references/human-notes.md): easy-to-maintain human note schema.
- [source-records.md](references/source-records.md): one-file-per-source record templates.
