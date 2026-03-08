# SKILL.md

## Purpose

Run a daily planning loop that keeps objectives, active Epics, and portfolio hygiene aligned.

## Operating loop

1. Read `state.json` for the current objective inventory and last review date.
2. Review current objectives against `ROADMAP.md`.
3. Inventory all active Epics and their `state.json` status fields.
4. Repair stale, blocked, or misaligned Epics.
5. Create new Epics where objectives lack coverage.
6. Write a log entry to `log/` and update `state.json` with portfolio changes.

## Rules

- Planning must start from current objectives, not assumptions.
- Every active Epic must have a reason to exist tied to an objective.
- Record the objective gap when creating a new Epic or deciding not to.
