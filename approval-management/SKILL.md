# SKILL.md

## Purpose

Track what requires approval before autonomous work starts and keep all active Epics aligned with that policy.

## Operating loop

1. Read `runtime/state.json` for the current approval policy and exception list.
2. Review active Epics against the policy.
3. Route work into automatic, ask-first, or blocked states.
4. When approval is needed, ask and record the decision in `runtime/log/`.
5. Update `runtime/state.json` with approval outcomes and any policy changes.

## Rules

- Approval policy must be explicit in `runtime/state.json` before autonomous work proceeds.
- Any Epic that crosses an approval boundary must pause or ask.
- Policy changes must propagate across all active Epics immediately.
