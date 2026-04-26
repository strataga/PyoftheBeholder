# Py of the Beholder - Agent Guide

Python/Pygame remake work inspired by Eye of the Beholder. The global Codex playbook applies; this file only captures project-specific expectations.

## Project Shape

- Runtime: Python 3 with Pygame. Existing docs mention Python 3.7+, `pygame`, and `pandas`.
- Main entrypoint: `python3 main.py`.
- Code lives primarily in `src/`; design/data assets live in `docs/`, `data/`, `levels/`, and related CSV files.
- Treat CSV/data files as source-of-truth game content. Do not hardcode data in Python when a data table already owns it.

## Working Rules

- Preserve the grid-based dungeon crawler feel and existing renderer/input model unless Jason explicitly asks for a larger rewrite.
- Keep changes small and easy to inspect. This repo is better served by clear, direct Python than framework-heavy abstractions.
- When adding gameplay behavior, update the relevant data files, docs, or tools along with code so behavior stays reproducible.
- Do not commit proprietary Eye of the Beholder game assets or copied commercial content.

## Verification

- Prefer the smallest runnable check first:
  - `python3 main.py`
- If adding parsing or data-loading behavior, add or run a focused Python smoke script/tool that loads the touched data.
- If no automated test exists for the area, state the manual verification performed and the remaining gap.
