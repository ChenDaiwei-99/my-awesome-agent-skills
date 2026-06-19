---
name: kb-ingest
description: Ingest one source at a time into an Obsidian LLM knowledge base by creating source markdown records for PDFs, literature, GitHub repositories, web pages, or text files. Use when adding raw data to the KB, summarizing a PDF into a source record, documenting a GitHub repo with preserved links and commit context, or updating wiki links after ingestion.
---

# KB Ingest

Use this skill to turn a raw source into one durable markdown source record. The record should be useful for local search and summary-level reasoning, while preserving original links so future agents can retrieve deeper details online.

## Workflow

1. Read the vault root `AGENTS.md` and follow any project-specific schema.
2. Identify the source kind: PDF, GitHub repository, web page, text/markdown file, or other.
3. Collect metadata, original URLs, local paths, publication dates, authors, repository owner/name, branch, and commit when available.
4. Inspect the source content carefully enough to write a faithful source record.
5. Create exactly one markdown record under the matching `sources/` folder using [source-record-template.md](references/source-record-template.md).
6. For PDFs, follow [pdf-ingest.md](references/pdf-ingest.md).
7. For GitHub repositories, follow [github-ingest.md](references/github-ingest.md).
8. Preserve all website links in `## Source Links` or `## Important Details`.
9. Add `## Links Into Wiki` entries only for existing or newly created wiki pages.
10. Update `wiki/index.md` and `wiki/log.md` directly or invoke the index/log workflow if available.
11. If contradictions appear, append them to `wiki/review.md`; do not rewrite human notes or contested wiki claims.

## Writing Requirements

- Write concrete summaries, not promotional blurbs.
- Separate `Summary`, `Key Takeaways`, `Keywords and Concepts`, `Important Details`, and `Open Questions`.
- Keep human-authored notes in `notes/` untouched unless the user explicitly asks for edits.
- Prefer Obsidian wikilinks for local KB pages and normal markdown links for external URLs.

## References

- [source-record-template.md](references/source-record-template.md): shared source record template.
- [pdf-ingest.md](references/pdf-ingest.md): PDF and literature ingestion.
- [github-ingest.md](references/github-ingest.md): GitHub repository ingestion.
