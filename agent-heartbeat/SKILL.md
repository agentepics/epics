# SKILL.md

## Purpose

Wake the agent on a regular interval. What happens each heartbeat is determined by the agent's other active Epics and standing instructions — this Epic only owns the cadence.

## Operating loop

1. Wake on schedule. Read `runtime/state.json` for cadence and last run time.
2. Hand control to the agent to act on whatever is current.
3. When the agent finishes its work, write a log entry to `runtime/log/`.
4. Update `runtime/state.json` with the completed run time and next scheduled wake.

## Rules

- This Epic manages the clock, not the work.
- Every wake must update `runtime/state.json` so the next interval is known.
- If the agent has nothing to do, log that and schedule the next wake anyway.
