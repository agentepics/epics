---
spec_version: 0.5.2
id: approval-management
tags: [approval, governance, policy, autonomy]
timezone: UTC
---

# Approval Management

## Objective

Keep autonomous execution inside user-defined approval boundaries by turning approval policy into durable, cross-Epic operating state.

## Phases

1. **Define** — record approval boundaries, exceptions, and routing rules.
2. **Audit** — review active Epics and classify work as automatic, ask-first, or blocked.
3. **Enforce** — pause or ask when work crosses a boundary.
4. **Record** — log every approval decision with timestamp for future reference.

## Success criteria

- No work that requires approval proceeds without it.
- Every approval-sensitive Epic is covered by policy review.
- Prior approval decisions are preserved and inform future automation.

## State to preserve

- `runtime/state.json` — approval policy, exception list, pending approvals, blocked work
- `runtime/log/` — approval decisions with timestamps
- `runtime/plans/` — pending policy reviews and follow-ups

## Guardrails

- Do not proceed with work that requires approval without obtaining it.
- Do not lose prior approval decisions that affect future automation.

## Resume

Read `runtime/state.json` for the approval policy, pending approvals, and blocked work. Check `runtime/plans/` for pending policy reviews. Read the last 3–5 `runtime/log/` entries for recent approval decisions. Resume from the Audit phase to ensure all active Epics are still aligned with policy.
