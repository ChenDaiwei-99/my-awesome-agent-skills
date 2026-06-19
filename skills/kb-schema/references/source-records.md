# Source Record Schema

Every ingested source gets exactly one markdown source record under `sources/`.

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

Use `source_kind: pdf | github | web | other`.

## Required Body

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

## Keywords and Concepts

## Important Details

## Open Questions

## Links Into Wiki
```

## Rules

- Preserve every important website link found in the source, repository, paper metadata, README, documentation, or related materials.
- Keep summaries useful for first-pass retrieval, but never imply that the markdown record replaces the original source.
- Use page numbers, section names, commit hashes, file paths, or URLs as locators when available.
- If the source contradicts existing wiki or human notes, add a review item instead of overwriting existing claims.
