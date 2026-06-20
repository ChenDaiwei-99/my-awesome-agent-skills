---
name: kb-lint
description: Audit an Obsidian LLM knowledge base and personal note space for structure, links, stale summaries, duplicate concepts, weak citations, unresolved contradictions, project-note consistency, and human/agent ownership violations. Use when checking workspace health, reviewing whether personal notes and sources are consistent, preparing cleanup work, or finding issues that should be added to knowledge-base/wiki/review.md.
---

# KB Lint

Use this skill to inspect knowledge-base health without making risky rewrites.

## Workflow

1. Read the vault root `AGENTS.md`.
2. Confirm the expected folders and control files exist.
3. Check human-owned `personal-notes/` for schema drift only; do not edit them during lint.
4. Check raw-source records for required frontmatter, required body sections, preserved links, and source locators.
5. Check wiki pages for citations back to raw-source records or human notes.
6. Search for duplicate concepts, orphan synthesis pages, broken wikilinks, and missing backlinks.
7. Identify contradictions or stale claims and route them to `knowledge-base/wiki/review.md`.
8. Produce a prioritized report with concrete file paths and suggested fixes.

## Checks

Use [lint-checks.md](references/lint-checks.md) for the full checklist.

## Fix Policy

- Apply low-risk mechanical fixes in the knowledge base only when the user asks for direct cleanup.
- Apply `personal-notes/` link/frontmatter formatting fixes directly when they are low-risk.
- For substantive `personal-notes/` fixes, list exact proposed changes and ask for permission before editing.
- Do not rewrite personal notes by default.
- Do not resolve contradictory claims automatically.
- Prefer review items over silent changes when evidence is ambiguous.

## Output

Group findings by severity:

- `Critical`: broken schema, missing raw-source records, or ownership violations.
- `High`: contradictions, missing citations, or important dead links.
- `Medium`: duplicate concepts, orphan wiki pages, weak summaries.
- `Low`: naming drift, minor frontmatter gaps, index freshness.
