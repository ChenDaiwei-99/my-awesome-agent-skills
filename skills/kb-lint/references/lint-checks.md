# KB Lint Checks

## Structure

- Root `AGENTS.md` exists.
- `notes/`, `sources/`, and `wiki/` exist.
- `wiki/index.md`, `wiki/log.md`, and `wiki/review.md` exist.
- `wiki/note-advice/` exists if advisory reports are saved.

## Human Notes

- Human notes stay under `notes/`.
- Human notes use lightweight frontmatter when present.
- Agent-generated advisory text is not inserted into human notes unless explicitly requested.

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
- Contradictory claims are copied or summarized into `wiki/review.md`.
- Stale claims with newer source records are flagged, not overwritten.

## Link Health

- Broken wikilinks are listed.
- External links that are central to source identity are checked when network access is available.
- Missing backlinks from source records to wiki pages are suggested.
