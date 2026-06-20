# GitHub Repository Ingestion

Represent each GitHub repository with one source markdown record under `knowledge-base/sources/github/`.

## Required Output

The source record must include:

- Repository URL.
- Owner and repository name.
- Branch and commit hash when available.
- Project purpose and maturity.
- Key takeaways.
- Keywords and concepts.
- Important files, directories, APIs, or modules.
- Setup, usage, or integration details if relevant.
- Preserved links to docs, releases, issues, PRs, examples, papers, project sites, and package registries.

## Process

1. Resolve the canonical repository URL.
2. Capture commit hash or branch. If using the live default branch, say so.
3. Inspect README, docs, package manifests, examples, tests, and top-level structure.
4. Follow important outbound links and preserve them, especially documentation and paper links.
5. Create `knowledge-base/sources/github/owner-repo.md`.
6. If a local checkout or archive exists, include its path in `local_path`.
7. Do not vendor or delete repository files unless the user explicitly asks.

## Suggested Body Additions

After the standard source record sections, add any useful GitHub-specific sections:

```markdown
## Repository Map

## Important Files and Modules

## Setup and Usage

## API or Interface Notes
```
