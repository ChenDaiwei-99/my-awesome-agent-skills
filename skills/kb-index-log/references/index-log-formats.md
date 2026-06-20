# Index, Log, and Review Formats

## knowledge-base/wiki/index.md

```markdown
# Knowledge Base Index

## Sources
- [[knowledge-base/sources/pdfs/example-paper]]
- [[knowledge-base/sources/github/owner-repo]]

## Concepts
- [[knowledge-base/wiki/concepts/example-concept]]

## Entities
- [[knowledge-base/wiki/entities/example-entity]]

## Syntheses
- [[knowledge-base/wiki/syntheses/example-topic]]

## Personal Notes Entry Points
- [[personal-notes/fleeting/example-note]]
- [[personal-notes/projects/example-project/timeline]]
- [[personal-notes/permanent/principles/example-principle]]

## Advisory Reports
- [[knowledge-base/wiki/note-advice/example-note-review]]
```

Keep the index curated. It should help the user navigate major knowledge areas.

## knowledge-base/wiki/log.md

Append entries in reverse chronological or chronological order according to the existing file. If the file is empty, use chronological order.

```markdown
# KB Log

- YYYY-MM-DD HH:mm - Ingested [[knowledge-base/sources/pdfs/example-paper]]; updated [[knowledge-base/wiki/index]].
```

## knowledge-base/wiki/review.md

```markdown
# KB Review Queue

## YYYY-MM-DD - Short issue title
- Status: open
- Trigger:
- Affected files:
- Evidence:
- Suggested resolution:
- Owner:
```

Review items are for claims or decisions that should not be resolved silently.

## Advisory Report Registry

When saving an advisor report, add it to the index and log:

```markdown
- YYYY-MM-DD HH:mm - Saved note advice [[knowledge-base/wiki/note-advice/example-note-review]] for [[personal-notes/projects/example-project/notes]].
```
