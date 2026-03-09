---
enabled: true
type: prompt
timeout: 180
---

An Epic has become blocked.
Check runtime/state.json to determine if the block is approval-related.
If the block requires user approval, add it to pending_approvals in runtime/state.json and log the request.
If the block is not approval-related, log it as an external block and take no approval action.
