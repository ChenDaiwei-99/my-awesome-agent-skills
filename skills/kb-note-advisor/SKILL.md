---
name: kb-note-advisor
description: Review human-written Obsidian notes against the knowledge base like an experienced advisor, identifying incomplete understanding, contradictions, missing evidence, and precise suggested revisions without editing the user's notes. Use when the user asks for critique, advice, review, correction, or deeper evaluation of their own notes using sources and wiki knowledge.
---

# KB Note Advisor

Use this skill to review the user's own notes against the knowledge base. Act as an experienced advisor: careful, concrete, precise, and evidence-grounded. Do not act as an automatic editor.

## Workflow

1. Read the target human note in `notes/`.
2. Extract its main claims, assumptions, interpretations, examples, and open questions.
3. Search relevant `sources/` records by wikilinks, tags, keywords, titles, concepts, and entities.
4. Search relevant `wiki/` concept, entity, synthesis, review, and prior advice pages.
5. Compare the note against source summaries, key takeaways, important details, wiki synthesis, and preserved source links.
6. If local records are too thin and the user asked for deep checking, follow preserved website links from source records.
7. Produce advisory feedback. Do not rewrite the original note unless the user explicitly asks for an edit.
8. Save a durable report under `wiki/note-advice/` only when requested.

## Advisory Standard

- Be detailed enough to be useful, but keep every point precise.
- Quote or paraphrase the note's claim before judging it.
- Explain why a claim is supported, incomplete, possibly wrong, or under-evidenced.
- Cite source records, wiki pages, human notes, and external URLs.
- Suggest exact revisions or next investigations.
- Distinguish factual contradiction from missing nuance.
- Treat personal experience as scoped evidence, not automatically as a mistake.

## Required Output Sections

Use this structure for normal reviews:

```markdown
# Advisory Review: Note Title

## Likely Correct

## Possibly Incomplete

## Possibly Wrong or Contradictory

## Missing Evidence or Sources

## Suggested Revisions

## Questions Worth Investigating
```

For each finding, include:

- `Note claim`: the claim or assumption being reviewed.
- `Assessment`: what is missing, wrong, or strong.
- `Evidence`: local source/wiki links and external links when used.
- `Suggested revision`: concrete replacement wording or next edit.
- `Confidence`: high, medium, or low.

## Persistence

When saving a report:

- Write it to `wiki/note-advice/YYYY-MM-DD-note-slug-review.md`.
- Link back to the reviewed human note.
- Link to the source records and wiki pages used.
- Update `wiki/index.md` and append to `wiki/log.md`.
- Add unresolved contradictions to `wiki/review.md`.

## Reference

- [advice-report.md](references/advice-report.md): durable advisory report template and review heuristics.
