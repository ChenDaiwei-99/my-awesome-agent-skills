# PDF Ingestion

Create one source record for each PDF.

## Required Output

The markdown record must include:

- A faithful `Summary`.
- A concrete `Key Takeaways` list.
- A `Keywords and Concepts` list suitable for search and linking.
- Important details with page, section, figure, or table locators when available.
- Original URL, DOI, arXiv page, publisher page, and local PDF path when available.

## Process

1. Identify title, authors, publication date, venue, DOI, arXiv ID, and original URL from the PDF or surrounding metadata.
2. Extract text using available local tools. If extraction is partial, say so in `Open Questions`.
3. Read abstract, introduction, methods or design sections, results, conclusion, and limitations before summarizing.
4. Preserve links from the paper body, references, project pages, supplements, and code repositories when they are relevant.
5. Write a source record under `knowledge-base/sources/pdfs/`.
6. Link related wiki concept or entity pages in `Links Into Wiki`.

## Local Files

If the PDF is stored in the vault, prefer:

```text
knowledge-base/raw/pdfs/original-file-name.pdf
```

Do not move, rename, or delete a user's PDF unless they asked for file organization.
