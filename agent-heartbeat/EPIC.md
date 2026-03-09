---
spec_version: 0.5.1
id: agent-heartbeat
tags: [scheduler, heartbeat, autonomy, roadmap]
timezone: UTC
---

# Agent Heartbeat

## Objective

Provide a durable wake-up cadence so the agent can act on its own schedule without manual prompting. This Epic does not prescribe what the agent does — only that it wakes up.

## Phases

1. **Configure** — set the cadence and record it in `runtime/state.json`.
2. **Run** — wake on schedule, hand control to the agent, record that a heartbeat occurred.

## Success criteria

- Heartbeats fire at the configured cadence.
- Every heartbeat is logged regardless of whether the agent had work to do.
- `runtime/state.json` always reflects the last and next scheduled wake.

## State to preserve

- `runtime/state.json` — cadence, last run time, next run time
- `runtime/log/` — one entry per heartbeat

## Guardrails

- Do not decide what work to do — that belongs to other Epics.
- Do not skip a scheduled wake without logging why.

## Resume

Read `runtime/state.json` for the cadence and last run time. Compute whether a heartbeat is overdue. Read the last 3–5 `runtime/log/` entries to confirm recent wake history. Resume the cadence from the current interval.
