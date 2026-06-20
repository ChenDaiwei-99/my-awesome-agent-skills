---
name: research-code-style
description: Initialize empty Python research repositories or review populated Python research repositories for minimal style, importable src modules, run_scripts shell launchers, uv-based commands, and clean experiment folders. Use for new empty research repos, AGENTS.md coding rules, or repository-structure reviews. For non-empty repos, review only; do not directly modify, move, delete, or reorganize files.
---

# Research Code Style

Use this skill to initialize empty research repos or review populated ones against a minimal Python research-code standard.

## Workflow

1. Decide the mode:
   - Empty repo: initialize a minimal layout.
   - Populated repo: review only; do not edit files.
2. Read local context first: `AGENTS.md`, `pyproject.toml`, README files, and existing module patterns.
3. Apply [rule-of-thumbs.md](references/rule-of-thumbs.md).
4. Do not hand-create `pyproject.toml` or `uv.lock`; the user initializes them with `uv init`.
5. Do not run expensive training or experiment commands unless the user explicitly asks.

## Output

- Empty repo: create only the minimal source/layout skeleton.
- Populated repo: return findings with paths, risks, and suggested moves.
- AGENTS request: return a concise `AGENTS.md` section from the reference.
