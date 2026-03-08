---
enabled: true
type: prompt
timeout: 120
---

This is the first activation of Agent Heartbeat.
Read state.json and configure the default cadence if not already set.
Verify cron.d/heartbeat.yml is enabled.
Write an initial log entry to log/ confirming the heartbeat schedule is active.
Update state.json with the first scheduled next_run time.
