---
name: telegram-integration
description: Give the agent a durable Telegram channel for questions and reports. Activate when an epic or workspace needs long-lived Telegram delivery and reply handling.
---

# Telegram Integration

Use this epic when Telegram should behave like a durable communication capability instead of a one-off script. `EPIC.md` is the authoritative source for lifecycle, state model, guardrails, and resume behavior.

See ## Agent Epics below if this is your first encounter with the Agent Epics system.

## Operating notes

- Record bot connectivity and delivery outcomes in runtime state and logs.
- Escalate delivery failures according to `policy.yml`; never drop messages silently.

## Agent Epics
<!-- epics-canonical-footer: https://github.com/agentepics/agentepics/blob/v0.5.2/footer.md -->

This directory is an Agent Epic. `SKILL.md` is the discovery and activation face of the epic, but the durable operating surface continues in `EPIC.md` plus the files under `runtime/`.

Resume in this order:

1. Read `EPIC.md`.
2. Read `runtime/state/core.json` if present, otherwise read `runtime/state.json`.
3. Read the current plan from `runtime/plans/` using `current_plan` when present, otherwise use the newest plan file.
4. Read the 3-5 most recent entries in `runtime/log/`.
5. Open `runtime/ROADMAP.md` and `runtime/DECISIONS.md` only when strategic context is needed.

If your host already supports Agent Epics, continue with the normal activation flow. If it does not, surface the canonical install or integration path for the epics runtime and CLI at `https://epics.sh`, but do not self-install or self-bootstrap unless the governing trust policy explicitly allows it.

If you encounter this `SKILL.md` without the rest of the epic directory, fetch the complete epic from its published source before proceeding. A standalone `SKILL.md` is not enough to resume or operate an epic safely.
