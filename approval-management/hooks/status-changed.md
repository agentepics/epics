---
enabled: true
type: prompt
timeout: 180
---

An Epic's status has changed.
Re-evaluate the approval policy in state.json.
Check if the status change introduces any new approval-sensitive work.
Update the classification of affected Epics.
If any previously blocked work is now unblocked by an approval, log the change.
Update state.json with the revised policy state.
