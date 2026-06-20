# Source Record Template

Create one markdown source record per source.

## Paths

- PDF or literature: `knowledge-base/sources/pdfs/YYYY-MM-DD-short-title.md`
- GitHub repository: `knowledge-base/sources/github/owner-repo.md`
- Web page: `knowledge-base/sources/web/YYYY-MM-DD-short-title.md`
- Other source: `knowledge-base/sources/other/YYYY-MM-DD-short-title.md`

## Frontmatter

```yaml
---
type: source
source_kind: pdf
title:
authors: []
created:
ingested: YYYY-MM-DD
status: active
source_url:
local_path:
repository:
commit:
tags: []
---
```

Use empty fields when unknown. Do not invent metadata.

## Body

```markdown
# Title

## Source Links
- Original:
- Local file:
- Repository:
- Commit:
- DOI:
- Related links:

## Summary

## Key Takeaways
- 

## Keywords and Concepts
- 

## Important Details
- 

## Open Questions
- 

## Links Into Wiki
- 
```

## Link Preservation

- Preserve original URLs, DOI URLs, arXiv URLs, GitHub URLs, documentation URLs, release URLs, issue or PR URLs, and project websites.
- If a URL appears important but was not used for the summary, still keep it under `Related links`.
- Use local paths under `knowledge-base/raw/` for downloaded PDFs, checked-out repositories, or stored attachments when available.
