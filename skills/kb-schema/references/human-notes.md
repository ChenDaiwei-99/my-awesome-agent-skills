# Human Note Schema

Human notes must remain easy to write manually. Use lightweight PARA-style folders and minimal frontmatter.

## Folders

- `notes/inbox/`: quick captures, drafts, and unprocessed ideas.
- `notes/projects/`: active outcomes with deadlines or deliverables.
- `notes/areas/`: ongoing responsibilities, interests, and practices.
- `notes/literature-notes/`: the user's own reading notes and reflections.
- `notes/journal/`: dated experience notes, observations, decisions, and personal logs.

## Default Frontmatter

```yaml
---
type: note
status: draft
created: YYYY-MM-DD
updated: YYYY-MM-DD
tags: []
---
```

## Optional Sections

Use these only when helpful:

```markdown
# Title

## Context

## My Understanding

## Evidence

## Questions

## Related
```

## Agent Rules

- Do not require IDs, backlinks, aliases, or atomic-note structure.
- Do not rewrite a human note without explicit permission.
- Prefer advisory comments, suggested replacement text, or a saved review under `wiki/note-advice/`.
- Add links or frontmatter only when the user asks for direct edits.
- Treat personal observations as evidence with scope, not as errors merely because they differ from literature.
