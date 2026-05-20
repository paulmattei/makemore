# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project state

This repo is currently an empty scaffold. `makemore.py`, `build_makemore.ipynb`, and `readme.md` are all 0 bytes; `main.py` is uv's default hello-world. There is no architecture to describe yet — when adding real code, update this file with the actual structure.

This repo is a working-through of Karpathy's "makemore" (character-level language modeling)

## Environment

- Python 3.13 (pinned in `.python-version`)
- Managed by [uv](https://docs.astral.sh/uv/); dependencies live in `pyproject.toml` and are locked in `uv.lock`
- Dev tools: `pyright` (type checking), `ruff` (lint/format)

## Commands

```bash
uv sync                 # install deps from uv.lock into .venv
uv run python main.py   # run the entry point
uv run ruff check .     # lint
uv run ruff format .    # format
uv run pyright          # type check
uv add <pkg>            # add a runtime dependency (updates pyproject.toml + lock)
uv add --dev <pkg>      # add a dev dependency
```

Prefer `uv run <cmd>` over activating the venv manually so the lockfile stays authoritative.
