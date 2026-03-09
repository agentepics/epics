---
enabled: true
type: prompt
timeout: 180
---

The coding loop has become blocked.
Read runtime/state.json and the current plan to understand the blocker.
Log the block with details about what is preventing progress.
Set blocked to true in runtime/state.json.
Check if the blocker can be resolved automatically (e.g., a failing test that needs investigation).
If not, escalate per policy.yml.
