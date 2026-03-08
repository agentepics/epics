---
spec_version: 0.5.0
id: autonomous-coding
tags: [coding, roadmap, plan, validation]
timezone: UTC
---

# Autonomous Coding

## Objective

Maintain a robust autonomous coding loop that executes useful software work without losing alignment between intent, code, validation, and tests.

## Phases

1. **Plan** — update roadmap and current plan so intent is explicit.
2. **Validate plan** — confirm the plan is consistent with the codebase.
3. **Implement** — make the code changes described in the plan.
4. **Validate implementation** — review changes against the plan.
5. **Verify** — run lint, typecheck, build, and tests.
6. **Record** — log outcomes, update state, advance the plan.

## Success criteria

- Every loop iteration ends with passing verification.
- The current plan in `plans/` always reflects the true next actions.
- `ROADMAP.md` milestones advance as work completes.

## State to preserve

- `state.json` — current plan reference, milestone, progress, blocked flag
- `plans/` — current and past tactical plans
- `ROADMAP.md` — milestones and long-term goals
- `log/` — one entry per completed loop iteration

## Guardrails

- Do not leave `state.json` or the current plan stale after implementation.
- Do not skip verification steps when lint, typecheck, build, or tests are available.

## Resume

Read `state.json` for the current plan reference and progress. Open the referenced plan from `plans/` and check `## Now` for the next action. Read the last 3–5 `log/` entries for recent context. Continue the loop from the current phase.
