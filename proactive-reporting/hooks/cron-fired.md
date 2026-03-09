---
enabled: true
type: prompt
timeout: 120
---

A cron job has completed. Check if the completed job was a reporting job. If delivery failed, add the report to the overdue list in runtime/state.json and log the failure. If delivery succeeded, clear any overdue flag for that report type. Update runtime/state.json.
