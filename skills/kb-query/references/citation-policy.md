# Citation Policy

Use citations to preserve the distinction between local notes, generated raw-source records, wiki synthesis, and external detail.

## Local Citations

- Personal note: `[[personal-notes/.../note-name]]`
- Raw-source record: `[[knowledge-base/raw/pdfs/paper-name]]`
- Wiki synthesis: `[[knowledge-base/wiki/syntheses/topic-name]]`
- Concept or entity: `[[knowledge-base/wiki/concepts/concept-name]]`

## External Citations

Use normal markdown links for external sources:

```markdown
[Project documentation](https://example.com/docs)
```

## Evidence Strength

Prefer this order for factual claims:

1. Original source URL, PDF, repository, or paper metadata.
2. Raw-source record with clear locator.
3. Wiki synthesis that cites raw-source records.
4. Human notes, clearly labeled as personal understanding or experience.

## Web Retrieval

If the user asks for more detail than the local KB contains, follow preserved URLs from raw-source properties or relevant details sections. Report when the retrieved information goes beyond the local record.

## Conflict Handling

When evidence conflicts:

- Cite both sides.
- Explain the difference precisely.
- Avoid overwriting either claim.
- Add or suggest a review item in `knowledge-base/wiki/review.md` if durable tracking is needed.
