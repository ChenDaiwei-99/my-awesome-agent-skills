# Standard Workspace Layout

Use this layout for new Obsidian-backed workspaces unless an existing vault schema says otherwise. It separates assistant-maintained external knowledge from human-owned personal notes.

```text
AGENTS.md

knowledge-base/
  raw/
    pdfs/
    github/
    web/
    other/
  wiki/
    index.md
    log.md
    review.md
    concepts/
    entities/
    syntheses/
    note-advice/

personal-notes/
  fleeting/
  projects/
    project-slug/
      timeline.md
      paper-survey.md
      ideas.md
      experiments.md
      notes.md
  permanent/
    advice/
    habits/
    principles/
```

## Ownership

| Area | Owner | Agent behavior |
| --- | --- | --- |
| `knowledge-base/raw/` | Agent maintained, human curated by request | Maintain one markdown raw-source record per external source. Preserve links and raw paths. Do not delete or reorganize records without explicit permission. |
| `knowledge-base/wiki/` | Agent | Maintain synthesis, indexes, logs, review queues, and advisory reports. |
| `personal-notes/fleeting/` | Human | Read and suggest processing. Apply link/frontmatter formatting directly; ask before substantive content changes. |
| `personal-notes/projects/` | Human | Read, cross-link, and suggest project structure. Apply link/frontmatter formatting directly; ask before substantive content changes. |
| `personal-notes/permanent/` | Human-owned, agent-assisted | Draft advice, habits, or principles; apply link/frontmatter formatting directly, but ask before writing substantive content. |
| `AGENTS.md` | Shared contract | Update only when schema or conventions intentionally change. |

## File Naming

- Use lowercase slugs for generated files.
- Use `knowledge-base/raw/pdfs/YYYY-MM-DD-short-title.md` for literature and PDF raw-source records when publication date or ingest date matters.
- Use `knowledge-base/raw/github/owner-repo.md` for GitHub repository raw-source records.
- Preserve human-chosen filenames in `personal-notes/`.
- Use `YYYY-MM-DD-short-title.md` for fleeting notes when a timestamp helps later processing.
- Use stable project slugs under `personal-notes/projects/`.

## Control Files

- `knowledge-base/wiki/index.md`: navigational map of major topics, source groups, and synthesis pages.
- `knowledge-base/wiki/log.md`: append-only maintenance log.
- `knowledge-base/wiki/review.md`: unresolved contradictions, missing evidence, and schema issues requiring human judgment.
- `knowledge-base/wiki/note-advice/`: durable reviews of personal notes when the user asks to save them.

## Personal Note Change Gate

Substantive modifications to `personal-notes/` require a separate approval step:

1. Read the relevant notes.
2. List the exact files to create, edit, rename, move, or delete.
3. Show the intended content changes or a concise patch-style summary.
4. Ask for permission and stop.
5. Apply changes only after the user approves.

This gate applies to new prose, rewritten claims, project scaffolding, permanent-note drafts, moves, renames, deletes, and nontrivial cleanup edits.

Link and frontmatter maintenance is exempt from the approval gate. Agents may directly add or repair wikilinks, backlinks, citation links, tags, aliases, dates, status fields, and other lightweight frontmatter/property formatting when the change does not alter the note's substantive claims.
