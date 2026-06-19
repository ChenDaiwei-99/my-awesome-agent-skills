---
name: kb-lint
description: Audit an Obsidian LLM knowledge base for structure, links, stale summaries, duplicate concepts, weak citations, unresolved contradictions, and human/agent ownership violations. Use when checking KB health, reviewing whether notes and sources are consistent, preparing cleanup work, or finding issues that should be added to wiki/review.md.
---

# KB Lint

Use this skill to inspect knowledge-base health without making risky rewrites.

## Workflow

1. Read the vault root `AGENTS.md`.
2. Confirm the expected folders and control files exist.
3. Check human-owned `notes/` for schema drift only; do not edit them unless explicitly asked.
4. Check source records for required frontmatter, required body sections, preserved links, and source locators.
5. Check wiki pages for citations back to source records or human notes.
6. Search for duplicate concepts, orphan synthesis pages, broken wikilinks, and missing backlinks.
7. Identify contradictions or stale claims and route them to `wiki/review.md`.
8. Produce a prioritized report with concrete file paths and suggested fixes.

## Checks

Use [lint-checks.md](references/lint-checks.md) for the full checklist.

## Fix Policy

- Apply low-risk mechanical fixes only when the user asks for direct cleanup.
- Do not rewrite human notes by default.
- Do not resolve contradictory claims automatically.
- Prefer review items over silent changes when evidence is ambiguous.

## Output

Group findings by severity:

- `Critical`: broken schema, missing source records, or ownership violations.
- `High`: contradictions, missing citations, or important dead links.
- `Medium`: duplicate concepts, orphan wiki pages, weak summaries.
- `Low`: naming drift, minor frontmatter gaps, index freshness.
