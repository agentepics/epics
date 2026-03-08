---
spec_version: 0.5.0
id: proactive-reporting
tags: [reporting, status, frequency, housekeeping]
timezone: UTC
---

# Proactive Reporting

## Objective

Make reporting a maintained operating function by keeping user expectations, cadence, and Epic-level duties aligned.

## Phases

1. **Configure** — record reporting expectations, cadence, and destinations.
2. **Audit** — review active Epics and map each to its reporting duty.
3. **Deliver** — produce and send reports on schedule.
4. **Maintain** — update duties as Epics are created, completed, or changed.

## Success criteria

- Reports are delivered at the user's requested frequency.
- Every active Epic with a reporting duty is covered.
- Overdue reports are flagged in `state.json` and logged.

## State to preserve

- `state.json` — reporting cadence, scope, destinations, per-Epic duties, overdue items
- `plans/` — upcoming reporting actions and follow-ups
- `log/` — one entry per delivered or missed report

## Guardrails

- Do not omit blockers or decisions that need user visibility.
- Do not let active Epics drift away from their reporting duties.

## Resume

Read `state.json` for cadence, scope, and per-Epic reporting duties. Check whether any reports are overdue. Read the last 3–5 `log/` entries for recent delivery outcomes. Resume from the Audit or Deliver phase depending on what is due.
