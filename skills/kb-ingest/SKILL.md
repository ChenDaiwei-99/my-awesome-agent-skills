---
name: kb-ingest
description: Ingest one external source at a time into an Obsidian LLM knowledge base by creating raw-source markdown records for PDFs, literature, GitHub repositories, web pages, or text files. Use when adding raw data to knowledge-base/raw, summarizing a PDF into knowledge-base/raw, documenting a GitHub repo with preserved links and commit context, or updating the LLM wiki after ingestion.
---

# KB Ingest

Use this skill to turn a raw source into one durable markdown raw-source record. The record should be useful for local search and summary-level reasoning, while preserving original links so future agents can retrieve deeper details online.

## Workflow

1. Read the vault root `AGENTS.md` and follow any project-specific schema.
2. Identify the source kind: PDF, GitHub repository, web page, text/markdown file, or other.
3. Collect metadata, original URLs, local paths, publication dates, authors, repository owner/name, branch, and commit when available.
4. Inspect the source content carefully enough to write a faithful raw-source record.
5. Create exactly one markdown record under the matching `knowledge-base/raw/` folder using [source-record-template.md](references/source-record-template.md).
6. For PDFs, follow [pdf-ingest.md](references/pdf-ingest.md).
7. For GitHub repositories, follow [github-ingest.md](references/github-ingest.md).
8. Preserve primary website links in raw-source properties and additional important links in `## Important Details`.
9. Add `## Links Into Wiki` entries only for existing or newly created wiki pages.
10. Update `knowledge-base/wiki/index.md` and `knowledge-base/wiki/log.md` directly or invoke the index/log workflow if available.
11. If contradictions appear, append them to `knowledge-base/wiki/review.md`; do not rewrite personal notes or contested wiki claims.

## Writing Requirements

- Write concrete summaries, not promotional blurbs.
- Separate `Summary`, `Key Takeaways`, `Keywords and Concepts`, `Important Details`, and `Open Questions`.
- Keep human-authored prose in `personal-notes/` untouched. Useful wikilinks, citation links, backlinks, or frontmatter/property formatting may be added directly; ask for permission before adding or rewriting substantive personal-note content.
- Prefer Obsidian wikilinks for local KB pages and normal markdown links for external URLs.

## References

- [source-record-template.md](references/source-record-template.md): shared raw-source record template.
- [pdf-ingest.md](references/pdf-ingest.md): PDF and literature ingestion.
- [github-ingest.md](references/github-ingest.md): GitHub repository ingestion.
