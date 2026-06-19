---
name: kb-query
description: Answer questions from an Obsidian LLM knowledge base using human notes, source records, and wiki synthesis with citations and preserved source links. Use when the user asks about knowledge stored in the KB, wants a research answer grounded in notes and sources, or asks for more detail that may require following preserved website links.
---

# KB Query

Use this skill to answer from the knowledge base while respecting the boundary between human notes, source records, and agent-maintained wiki pages.

## Workflow

1. Read the vault root `AGENTS.md` for schema, citation, and conflict rules.
2. Search `wiki/index.md`, `wiki/concepts/`, `wiki/entities/`, and `wiki/syntheses/` for existing synthesis.
3. Search `sources/` for source records with summaries, takeaways, keywords, and preserved links.
4. Search `notes/` for relevant human understanding, experiences, or interpretations.
5. Answer from local KB content first.
6. If the user asks for deeper detail and the local record is insufficient, follow preserved URLs from source records and cite the retrieved web detail.
7. Distinguish source-backed facts, wiki synthesis, and human-authored interpretation.
8. If evidence conflicts, state the conflict and cite both sides rather than resolving it silently.
9. If the user asks to save the answer, create or update a page under `wiki/syntheses/` and log it.

## Answer Style

- Be precise and evidence-grounded.
- Cite local pages with Obsidian links and external sources with markdown links.
- Use page, section, file path, commit, or URL locators when available.
- Say when the KB does not contain enough evidence.
- Do not rewrite human notes unless explicitly requested.

## Persistent Answers

When saving an answer:

- Place durable synthesis under `wiki/syntheses/`.
- Add related concepts or entities if the synthesis creates reusable knowledge.
- Update `wiki/index.md`.
- Append an entry to `wiki/log.md`.
- Route contradictions or missing evidence to `wiki/review.md`.

## Reference

- [citation-policy.md](references/citation-policy.md): citation and evidence handling.
