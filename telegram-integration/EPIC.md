---
spec_version: 0.5.0
id: telegram-integration
tags: [telegram, messaging, questions, reports]
timezone: UTC
---

# Telegram Integration

## Objective

Make autonomous work reachable by giving the agent a reliable Telegram path for questions, reports, and status updates.

## Phases

1. **Setup** — configure bot token, verify connectivity, record chat targets.
2. **Active** — route messages based on context: questions when blocked, reports on schedule.
3. **Maintenance** — update targets and preferences as the user directs.

## Success criteria

- Bot connection is verified and recorded in `state.json`.
- Messages reach the correct chat target without silent failures.
- Delivery failures are logged and escalated.

## State to preserve

- `state.json` — bot status, active chat targets, delivery preferences, question-vs-report policy
- `log/` — message delivery outcomes and failures

## Guardrails

- Do not send messages to the wrong chat target.
- Do not silently drop delivery failures.

## Resume

Read `state.json` for bot connection status and chat targets. If the bot is configured, the capability is ready — no further setup needed. Check `log/` for recent delivery failures that may need retry.
