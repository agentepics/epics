---
enabled: true
type: prompt
timeout: 120
---

The Telegram integration status has changed. If paused, log that message delivery is suspended -- other Epics should know not to route messages through Telegram. If reactivated, verify bot connectivity before resuming. Update runtime/state.json with the current connection state.
