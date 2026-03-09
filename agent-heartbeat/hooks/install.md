---
enabled: true
type: prompt
timeout: 120
---

This is the first activation of Agent Heartbeat.
Read runtime/state.json and configure the default cadence if not already set.
Verify cron.d/heartbeat.yml is enabled.
Write an initial log entry to runtime/log/ confirming the heartbeat schedule is active.
Update runtime/state.json with the first scheduled next_run time.
