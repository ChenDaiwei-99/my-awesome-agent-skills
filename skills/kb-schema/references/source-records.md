# Raw-Source Record Schema

Every ingested external source gets exactly one markdown raw-source record under `knowledge-base/raw/`. Raw files and snapshots live under `knowledge-base/raw/` and are treated as immutable.

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

Use `source_kind: pdf | github | web | other`.

## Required Body

```markdown
# Title

## Summary

## Key Takeaways

## Keywords and Concepts

## Important Details

## Open Questions

## Links Into Wiki
```

## Rules

- Preserve every important website link found in the source, repository, paper metadata, README, documentation, or related materials.
- Keep `source_url`, `local_file`, and `referred_by` in properties instead of duplicating them in the body.
- Keep summaries useful for first-pass retrieval, but never imply that the markdown record replaces the original source.
- Use page numbers, section names, commit hashes, file paths, or URLs as locators when available.
- If the source contradicts existing wiki or human notes, add a review item instead of overwriting existing claims.
- Link `personal-notes/projects/*/paper-survey.md` entries to raw-source records rather than duplicating source summaries. Adding or repairing these links is allowed directly; ask for approval before adding substantive survey prose.
