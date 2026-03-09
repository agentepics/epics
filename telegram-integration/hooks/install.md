---
enabled: true
type: prompt
timeout: 300
---

Telegram Integration is being installed. Check runtime/state.json for bot_token_set status. If the bot token is not configured, prompt the user to provide the Telegram bot token (via environment variable TELEGRAM_BOT_TOKEN). Once the token is available, verify connectivity by calling the Telegram getMe API. Record the bot username and connection status in runtime/state.json. Ask the user for the primary chat target (chat ID or username). Record chat_targets in runtime/state.json. Write a runtime/log entry confirming successful setup or documenting what still needs configuration.
