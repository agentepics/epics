---
enabled: true
type: prompt
timeout: 300
---

Proactive Reporting is being installed. Scan all active Epics in the workspace. For each Epic, determine if it should have reporting duties based on its category and status. Build the initial per_epic_duties map in state.json. Set default reporting cadence to daily if not specified. Prompt the user for reporting destinations (or note that destinations need configuration). Write an initial plan and log entry documenting the reporting setup.
