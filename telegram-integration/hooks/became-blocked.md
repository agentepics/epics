---
enabled: true
type: prompt
timeout: 180
---

The Telegram integration has become blocked. This likely means connectivity failed or the bot token is invalid. Read state.json for current bot status. Attempt to diagnose the issue -- check if the token is set, try a test API call. Log the failure details. If the bot cannot connect, set bot_configured to false in state.json and escalate per policy.yml.
