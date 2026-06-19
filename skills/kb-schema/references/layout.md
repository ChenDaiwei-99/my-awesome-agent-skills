# Standard Knowledge Base Layout

Use this layout for new Obsidian-backed LLM knowledge bases unless an existing vault schema says otherwise.

```text
AGENTS.md

notes/
  inbox/
  projects/
  areas/
  literature-notes/
  journal/

sources/
  pdfs/
  github/
  web/
  other/
  _files/
    pdfs/
    github/
    other/

wiki/
  index.md
  log.md
  review.md
  concepts/
  entities/
  syntheses/
  note-advice/
```

## Ownership

| Area | Owner | Agent behavior |
| --- | --- | --- |
| `notes/` | Human | Read, link, and suggest. Edit only with explicit permission. |
| `sources/` | Agent | Maintain one markdown source record per source. Preserve links and local paths. |
| `sources/_files/` | Human or agent | Store optional immutable local PDFs, repo snapshots, and attachments. Do not delete automatically. |
| `wiki/` | Agent | Maintain synthesis, indexes, logs, review queues, and advisory reports. |
| `AGENTS.md` | Shared contract | Update only when schema or conventions intentionally change. |

## File Naming

- Use lowercase slugs for generated files.
- Use `YYYY-MM-DD-short-title.md` for literature and PDF source records when publication date or ingest date matters.
- Use `owner-repo.md` for GitHub repository source records.
- Preserve human-chosen filenames in `notes/`.

## Control Files

- `wiki/index.md`: navigational map of major topics, source groups, and synthesis pages.
- `wiki/log.md`: append-only maintenance log.
- `wiki/review.md`: unresolved contradictions, missing evidence, and schema issues requiring human judgment.
- `wiki/note-advice/`: durable reviews of human notes when the user asks to save them.
