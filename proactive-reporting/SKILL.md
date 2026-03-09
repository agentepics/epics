# SKILL.md

## Purpose

Track what the user wants reported, how often, and keep active Epics aligned with those reporting duties.

## Operating loop

1. Read `runtime/state.json` for reporting cadence, scope, and per-Epic duties.
2. Review active Epics for reporting obligations.
3. Collect status signals: progress, blockers, and pending decisions.
4. Produce and send reports on schedule.
5. Write a log entry to `runtime/log/` and update `runtime/state.json` with delivery status.

## Rules

- Reporting frequency must follow the user's preference in `runtime/state.json`.
- Every report must separate progress, blockers, and asks.
- Log overdue or failed reports — never silently skip a cycle.
