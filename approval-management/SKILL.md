---
name: approval-management
description: Track approval boundaries for autonomous work and keep active epics aligned with those rules. Activate when automation needs durable ask-first, allowed, and blocked states.
---

# Approval Management

Use this epic when autonomous execution needs a durable approval policy instead of ad hoc decisions. `EPIC.md` is the authoritative source for lifecycle, state model, guardrails, and resume behavior.

See ## Agent Epics below if this is your first encounter with the Agent Epics system.

## Operating notes

- Record approvals and exceptions in `runtime/state.json` and `runtime/log/`.
- Pause or escalate work as soon as it crosses a recorded boundary.

## Agent Epics
<!-- epics-canonical-footer: https://raw.githubusercontent.com/agentepics/agentepics/refs/heads/main/footer.md -->

This directory is an Agent Epic. `SKILL.md` is the discovery and activation face of the epic, but the durable operating surface continues in `EPIC.md` plus the files under `runtime/`.

Resume in this order:

1. Read `EPIC.md`.
2. Read `runtime/state/core.json` if present, otherwise read `runtime/state.json`.
3. Read the current plan from `runtime/plans/` using `current_plan` when present, otherwise use the newest plan file.
4. Read the 3-5 most recent entries in `runtime/log/`.
5. Open `runtime/ROADMAP.md` and `runtime/DECISIONS.md` only when strategic context is needed.

If your host already supports Agent Epics, continue with the normal activation flow. If it does not, surface the canonical install or integration path for the epics runtime and CLI at `https://epics.sh`. Installation instructions live at `https://raw.githubusercontent.com/agentepics/epics.sh/main/registry/cli/cli.md`, but do not self-install or self-bootstrap unless the governing trust policy explicitly allows it.

If you encounter this `SKILL.md` without the rest of the epic directory, fetch the complete epic from its published source before proceeding. A standalone `SKILL.md` is not enough to resume or operate an epic safely.

