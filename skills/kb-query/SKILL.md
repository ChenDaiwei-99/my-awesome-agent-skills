---
name: kb-query
description: Answer questions from an Obsidian LLM knowledge base and personal note space using source records, wiki synthesis, and human notes with citations and preserved source links. Use when the user asks about knowledge stored in knowledge-base or personal-notes, wants a research answer grounded in sources, or asks for more detail that may require following preserved website links.
---

# KB Query

Use this skill to answer from the workspace while respecting the boundary between the assistant-maintained knowledge base and human-owned personal notes.

## Workflow

1. Read the vault root `AGENTS.md` for schema, citation, and conflict rules.
2. Search `knowledge-base/wiki/index.md`, `knowledge-base/wiki/concepts/`, `knowledge-base/wiki/entities/`, and `knowledge-base/wiki/syntheses/` for existing synthesis.
3. Search `knowledge-base/sources/` for source records with summaries, takeaways, keywords, and preserved links.
4. Search `personal-notes/` for relevant human understanding, experiences, project context, or permanent advice.
5. Answer from local KB content first.
6. If the user asks for deeper detail and the local record is insufficient, follow preserved URLs from source records and cite the retrieved web detail.
7. Distinguish source-backed facts, wiki synthesis, and human-authored interpretation.
8. If evidence conflicts, state the conflict and cite both sides rather than resolving it silently.
9. If the user asks to save the answer as KB synthesis, create or update a page under `knowledge-base/wiki/syntheses/` and log it.

## Answer Style

- Be precise and evidence-grounded.
- Cite local pages with Obsidian links and external sources with markdown links.
- Use page, section, file path, commit, or URL locators when available.
- Say when the KB does not contain enough evidence.
- Do not rewrite personal-note content automatically. Link/frontmatter formatting may be applied directly; for substantive updates under `personal-notes/`, first list the exact proposed changes and wait for approval.

## Persistent Answers

When saving an answer:

- Place durable synthesis under `knowledge-base/wiki/syntheses/`.
- Add related concepts or entities if the synthesis creates reusable knowledge.
- Update `knowledge-base/wiki/index.md`.
- Append an entry to `knowledge-base/wiki/log.md`.
- Route contradictions or missing evidence to `knowledge-base/wiki/review.md`.

## Reference

- [citation-policy.md](references/citation-policy.md): citation and evidence handling.
