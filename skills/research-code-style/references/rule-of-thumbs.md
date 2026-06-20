# Research Code Rule-of-Thumbs

## Code Style

- Keep Python direct, typed, and readable.
- Prefer small functions, dataclasses, typed dictionaries, and plain containers over heavy abstractions.
- Use type hints at public boundaries and for core state/configuration.
- Keep orchestration explicit: a small `main()` or `build_*` function assembles dependencies and starts work.
- Keep helper functions private when they are implementation details.
- Comment only on non-obvious assumptions, math, estimator choices, backend quirks, or fragile tradeoffs.
- Avoid hidden side effects at import time.

## Repository Shape

Preferred layout:

```text
repo/
  AGENTS.md
  pyproject.toml
  uv.lock
  .gitignore
  README.md
  run_scripts/
    train_baseline.sh
    eval_checkpoint.sh
  src/
    __init__.py
    training/
      __init__.py
      main.py
    evaluation/
      __init__.py
      main.py
    data/
    models/
    utils/
  datasets/
  outputs/
  .log/
```

Rules:

- Use this as an initializer for empty repos or a review standard for populated repos.
- Do not reshape a populated repo directly; report findings and suggested moves.
- Keep root free of `.py` files.
- Keep root limited to metadata, uv/Git config, docs, and optional `AGENTS.md`.
- Do not hand-create `pyproject.toml` or `uv.lock`; ask the user to run `uv init` when missing.
- Keep algorithms, models, data loading, metrics, training, evaluation, plotting, and utilities importable under `src/`.
- Keep entrypoint modules under `src/training/` or `src/evaluation/`.
- Keep generated artifacts outside source packages, usually in `.log/`, `datasets/`, and `outputs/`.

## Run Scripts

- Keep experiment launchers in `run_scripts/` as shell-style CLI command files.
- Let launchers choose hyperparameters, seeds, paths, and experiment names.
- Do not put Python logic, training loops, metrics, logging setup, or data transforms in launchers.
- Delegate to module entrypoints:

```bash
uv run python -m src.training.main \
  --learning-rate 1e-4 \
  --seed 42 \
  --output-dir outputs/baseline
```

## AGENTS.md Snippet

```md
## Coding Style

- Keep Python code minimal, typed, and directly readable.
- Prefer small functions and importable modules over large classes or script-only logic.
- Add type hints at public boundaries and for core research state/configuration.
- Use comments only for non-obvious assumptions, math choices, backend quirks, or fragile tradeoffs.

## Research Repository Structure

- Use these rules to initialize an empty repository or review a populated one.
- Do not directly reorganize a non-empty repository unless the user separately asks for specific edits.
- Keep algorithms, utilities, models, data loading, training, evaluation, metrics, and analysis helpers importable under `src/`.
- Keep repository root free of `.py` files.
- Put experiment launchers under `run_scripts/` as shell-style CLI command files.
- Keep launchers thin; they choose parameters and delegate to `src/training/` entrypoints.
- Keep `.log/`, `datasets/`, and `outputs/` beside `src/`.
- Do not hand-create `pyproject.toml` or `uv.lock`; ask the user to run `uv init` when project metadata is missing.
```
