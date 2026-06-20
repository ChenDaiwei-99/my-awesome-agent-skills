---
name: personal-note-distill
description: Distill fleeting notes, project notes, conversations, and knowledge-base material into reusable permanent personal notes such as advice, habits, principles, and high-level philosophy. Use when the user asks to process rough notes, extract lessons, create permanent notes, update personal principles, or turn project experience into durable guidance without losing links to the original evidence.
---

# Personal Note Distill

Use this skill to turn lived experience and accumulated knowledge into durable personal advice. The output belongs in the human-owned personal note space, so draft carefully. Link/frontmatter formatting can be applied directly, but do not write substantive permanent-note content until the user approves the exact proposed changes.

## Workflow

1. Read the relevant material from `personal-notes/fleeting/`, `personal-notes/projects/`, conversations supplied by the user, and `knowledge-base/`.
2. Identify recurring lessons, decision heuristics, habits, warnings, and high-level principles.
3. Search `personal-notes/permanent/` for existing related notes before creating a new one.
4. Link each candidate principle back to its origins: fleeting notes, project timeline entries, ideas, experiments, source records, wiki pages, or conversation excerpts.
5. Separate durable advice from temporary todos, project-specific facts, and unsupported speculation.
6. Draft a new permanent note or propose edits to an existing one.
7. Apply any needed link/frontmatter formatting directly when it only repairs structure.
8. List the exact substantive files and changes that would be made under `personal-notes/`.
9. Ask for permission and stop.
10. Apply substantive personal-note changes only after the user approves the listed changes.

## Permanent Note Standard

Permanent notes should be reusable by the user in future decisions. They should not merely summarize a source or project.

Use this structure:

```markdown
# Principle or Advice

## Advice

## When It Applies

## Why It Matters

## Evidence and Origin

## Practice Cues

## Related Notes
```

## Quality Bar

- Make the advice specific enough to guide behavior.
- Preserve nuance and limits; avoid universal claims from narrow evidence.
- Prefer "When X, do Y because Z" over abstract slogans.
- Include practical cues that help the user notice when the principle applies.
- Link to source records and project experiments when the advice depends on external knowledge.
- Link to fleeting or project notes when the advice comes from personal experience.
- Treat substantive output as a draft until the user approves writing it into `personal-notes/`.

## Reference

- [permanent-note-template.md](references/permanent-note-template.md): template and examples for permanent notes.
