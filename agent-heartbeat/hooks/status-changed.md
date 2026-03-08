---
enabled: true
type: prompt
timeout: 120
---

The heartbeat epic's status has changed.
If status is now "paused", note in state.json that heartbeats are suspended and log the pause.
If status is now "active", recompute the next_run time from the current moment and log the resumption.
Do not alter the cadence itself.
