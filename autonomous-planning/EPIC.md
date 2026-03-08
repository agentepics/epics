---
spec_version: 0.5.0
id: autonomous-planning
tags: [planning, inventory, housekeeping, objectives]
timezone: UTC
---

# Autonomous Planning

## Objective

Keep the Epic portfolio aligned with objectives through recurring autonomous planning and housekeeping.

## Phases

1. **Review** — read current objectives and compare to the active portfolio.
2. **Audit** — inventory all active Epics, flag stale or blocked ones.
3. **Repair** — fix misaligned Epics or mark them for removal.
4. **Expand** — create new Epics where objectives lack coverage.
5. **Record** — log decisions and update state.

## Success criteria

- Every planning cycle reviews all objectives and all active Epics.
- No stale Epic survives a cycle without justification.
- New Epics are traceable to a specific objective gap.

## State to preserve

- `state.json` — objective inventory, Epic portfolio snapshot, last review timestamp
- `plans/` — current planning actions and follow-ups
- `log/` — one entry per planning cycle with decisions made

## Guardrails

- Do not keep stale Epics alive without explicit justification.
- Do not create new Epics without recording the objective gap they cover.

## Resume

Read `state.json` for the objective inventory and last review date. Check `plans/` for pending planning actions. Read the last 3–5 `log/` entries to see recent portfolio decisions. Run the next planning cycle from the Review phase.
