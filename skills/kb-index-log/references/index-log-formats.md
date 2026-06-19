# Index, Log, and Review Formats

## wiki/index.md

```markdown
# Knowledge Base Index

## Sources
- [[sources/pdfs/example-paper]]
- [[sources/github/owner-repo]]

## Concepts
- [[wiki/concepts/example-concept]]

## Entities
- [[wiki/entities/example-entity]]

## Syntheses
- [[wiki/syntheses/example-topic]]

## Human Notes Entry Points
- [[notes/inbox/example-note]]

## Advisory Reports
- [[wiki/note-advice/example-note-review]]
```

Keep the index curated. It should help the user navigate major knowledge areas.

## wiki/log.md

Append entries in reverse chronological or chronological order according to the existing file. If the file is empty, use chronological order.

```markdown
# KB Log

- YYYY-MM-DD HH:mm - Ingested [[sources/pdfs/example-paper]]; updated [[wiki/index]].
```

## wiki/review.md

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
- YYYY-MM-DD HH:mm - Saved note advice [[wiki/note-advice/example-note-review]] for [[notes/areas/example-note]].
```
