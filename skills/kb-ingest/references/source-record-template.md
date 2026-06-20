# Raw-Source Record Template

Create one markdown raw-source record per source.

## Paths

- PDF or literature: `knowledge-base/raw/pdfs/YYYY-MM-DD-short-title.md`
- GitHub repository: `knowledge-base/raw/github/owner-repo.md`
- Web page: `knowledge-base/raw/web/YYYY-MM-DD-short-title.md`
- Other source: `knowledge-base/raw/other/YYYY-MM-DD-short-title.md`

## Frontmatter

```yaml
---
type: raw-source
source_kind: pdf
title:
summary_status: pending
source_url:
captured: YYYY-MM-DD
status: pointer-only
local_file:
referred_by: []
tags: []
---
```

Use empty fields when unknown. Do not invent metadata.

## Body

```markdown
# Title

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
- Keep the primary source URL in `source_url`; use `Important Details` for additional URLs that matter to interpretation.
- Use `local_file` for downloaded PDFs, checked-out repositories, or stored attachments when available.
