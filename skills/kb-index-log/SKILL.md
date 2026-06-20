---
name: kb-index-log
description: Maintain Obsidian LLM knowledge-base index, log, review queue, and advisory-report registry files. Use when adding raw-source records, filing synthesis pages, recording KB maintenance actions, appending unresolved contradictions to knowledge-base/wiki/review.md, or keeping knowledge-base/wiki/index.md navigable.
---

# KB Index Log

Use this skill to keep the knowledge base navigable and auditable.

## Responsibilities

- Maintain `knowledge-base/wiki/index.md` as a topic-oriented map, not a dump of every file.
- Maintain `knowledge-base/wiki/log.md` as append-only chronological history.
- Maintain `knowledge-base/wiki/review.md` as the queue for contradictions, missing evidence, stale claims, and user decisions.
- Track saved note-advisor reports under `knowledge-base/wiki/note-advice/`.

## Workflow

1. Read `AGENTS.md` for local index and log preferences.
2. Add or update index links after creating raw-source records, concept pages, entity pages, synthesis pages, or advisory reports.
3. Append a log entry for every meaningful maintenance action.
4. Append review items for unresolved contradictions or decisions.
5. Keep entries concise, dated, and linked to affected files.
6. Do not rewrite old log entries except to fix broken markdown syntax.

## Formats

Use [index-log-formats.md](references/index-log-formats.md) for file templates and entry formats.

## Rules

- Prefer stable Obsidian wikilinks for local pages.
- Keep external URLs in raw-source records, not as scattered index clutter, unless the URL is itself a major resource.
- Do not remove review items until the user or a later workflow resolves them.
