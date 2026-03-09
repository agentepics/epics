# SKILL.md

## Purpose

Give the agent a durable Telegram channel for asking questions and sending reports. This is a capability Epic — once installed, the agent has Telegram the way it has bash.

## Operating loop

1. Check `runtime/state.json` for bot connection status and active chat targets.
2. If not configured, set up Telegram bot connectivity and record targets.
3. When another Epic or the agent needs to communicate, decide: question or report.
4. Send the message and record the outcome in `runtime/log/`.
5. On failure, log the failure and escalate per `policy.yml`.

## Rules

- Only ask questions when they materially block progress.
- Follow the user's reporting preferences stored in `runtime/state.json`.
- Log every delivery failure — never silently drop a message.
