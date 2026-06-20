# Personal Note Schema

Personal notes must remain easy to write manually. The structure has three levels: fleeting notes, project notes, and permanent notes.

## Folders

- `personal-notes/fleeting/`: quick captures, meeting notes, temporary thoughts, quick todos, and rough observations.
- `personal-notes/projects/`: project-based notes.
- `personal-notes/permanent/`: distilled reusable advice, habits, principles, and high-level philosophy.

## Fleeting Notes

```yaml
---
type: fleeting-note
created: YYYY-MM-DD
updated: YYYY-MM-DD
tags: []
---
```

Use any simple body structure. These notes optimize for capture speed, not polish.

Common sections:

```markdown
# Title

## Raw Notes

## Todos

## Follow Up

## Questions
```

## Project Notes

Each project lives under:

```text
personal-notes/projects/project-slug/
  timeline.md
  paper-survey.md
  ideas.md
  experiments.md
  notes.md
```

Project files should use lightweight frontmatter:

```yaml
---
type: project-note
project: project-slug
created: YYYY-MM-DD
updated: YYYY-MM-DD
status: active
tags: []
---
```

Use these files consistently:

- `timeline.md`: project schedule, milestones, deadlines, meetings, and decisions.
- `paper-survey.md`: relevant papers and raw-source records linked to `knowledge-base/raw/` or `knowledge-base/wiki/`.
- `ideas.md`: potential ideas to try, each with a stable heading or block ID.
- `experiments.md`: experiment plans, runs, results, and links back to ideas.
- `notes.md`: miscellaneous project context that does not yet fit elsewhere.

Double-link ideas and experiments:

```markdown
## Idea: Contrastive Baseline Sweep ^idea-contrastive-baseline

Related experiments:
- [[experiments#Experiment: Baseline Sweep]]
```

```markdown
## Experiment: Baseline Sweep

Tests: [[ideas#^idea-contrastive-baseline]]
```

## Permanent Notes

Permanent notes capture reusable advice for the user: habits, principles, decision heuristics, research taste, collaboration patterns, or personal philosophy.

```yaml
---
type: permanent-note
created: YYYY-MM-DD
updated: YYYY-MM-DD
derived_from: []
tags: []
---
```

Use this body shape when helpful:

```markdown
# Principle or Advice

## Advice

## When It Applies

## Why It Matters

## Evidence and Origin

## Related Notes
```

## Agent Rules

- Do not require IDs, backlinks, aliases, or atomic-note structure.
- Do not modify substantive content under `personal-notes/` automatically.
- Link and frontmatter maintenance may be applied directly when it only adds or repairs wikilinks, backlinks, citation links, tags, aliases, dates, status fields, or other lightweight property formatting.
- Before creating, editing, moving, renaming, deleting, or rewriting substantive personal-note content, list the exact proposed changes and ask for permission.
- Apply substantive personal-note changes only after the user approves the listed changes.
- Prefer advisory comments, suggested replacement text, or a saved review under `knowledge-base/wiki/note-advice/`.
- Treat project scaffolding and permanent-note drafts as substantive changes that require the approval gate.
- Treat personal observations as evidence with scope, not as errors merely because they differ from literature.
- Draft permanent notes only when the user asks for distillation, reflection, or reusable advice; ask again before writing the draft into `personal-notes/permanent/`.
