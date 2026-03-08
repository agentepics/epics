---
enabled: true
type: prompt
timeout: 120
---

The autonomous coding epic's status has changed. Read state.json for the current
status. If paused, log that the coding loop is suspended and set blocked to true
so cron does not attempt work. If resumed to active, set blocked to false,
revalidate the current plan against the codebase, and log the resumption. If
marked complete, write a final log entry summarizing total progress and milestone
completion.
