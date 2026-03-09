---
enabled: true
type: prompt
timeout: 300
---

Approval Management is being installed.
Scan all active Epics in the workspace to build an initial inventory.
For each Epic, classify its work as "automatic" (no approval needed), "ask-first" (pause and ask before proceeding), or "blocked" (cannot proceed at all).
Record the initial approval policy in runtime/state.json.
Write a log entry documenting the initial policy and which Epics were classified under each category.
