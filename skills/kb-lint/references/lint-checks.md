# KB Lint Checks

## Structure

- Root `AGENTS.md` exists.
- `knowledge-base/raw/`, `knowledge-base/sources/`, `knowledge-base/wiki/`, and `personal-notes/` exist.
- `knowledge-base/wiki/index.md`, `knowledge-base/wiki/log.md`, and `knowledge-base/wiki/review.md` exist.
- `knowledge-base/wiki/note-advice/` exists if advisory reports are saved.
- `personal-notes/fleeting/`, `personal-notes/projects/`, and `personal-notes/permanent/` exist.

## Human Notes

- Personal notes stay under `personal-notes/`.
- Personal notes use lightweight frontmatter when present.
- Agent-generated advisory text is not inserted into personal notes automatically.
- Link/frontmatter fixes under `personal-notes/` may be applied directly when they only repair wikilinks, backlinks, citation links, tags, aliases, dates, status fields, or lightweight properties.
- Substantive proposed `personal-notes/` writes include an exact file/change list and wait for user approval before modification.
- Working projects contain `timeline.md`, `paper-survey.md`, `ideas.md`, `experiments.md`, and `notes.md` unless the local schema overrides this.
- Project `paper-survey.md` files link to knowledge-base source records instead of duplicating long summaries.
- Project ideas and experiments are double-linked when one tests or depends on the other.
- Permanent notes include enough origin links to trace the fleeting notes, project notes, conversation, or KB material they were distilled from.

## Source Records

- Each source record has `type: source`.
- `source_kind` is one of `pdf`, `github`, `web`, or `other`.
- Required sections exist: `Source Links`, `Summary`, `Key Takeaways`, `Keywords and Concepts`, `Important Details`, `Open Questions`, `Links Into Wiki`.
- Important external URLs are preserved.
- Local paths, repository URLs, commits, DOIs, or page locators are included when known.

## Wiki Pages

- Synthesis pages cite source records or human notes.
- Concept and entity pages link back to relevant source records.
- Index entries point to existing files.
- Log entries are append-only and dated.

## Evidence Quality

- Claims with no source, note, URL, or locator are flagged.
- Duplicate concepts with overlapping meaning are flagged.
- Contradictory claims are copied or summarized into `knowledge-base/wiki/review.md`.
- Stale claims with newer source records are flagged, not overwritten.

## Link Health

- Broken wikilinks are listed.
- External links that are central to source identity are checked when network access is available.
- Missing backlinks from source records to wiki pages are suggested.
