# SKILL.md

## Purpose

Run an autonomous coding loop that keeps roadmap, plan, implementation, validation, and tests aligned.

## Operating loop

1. Read `runtime/state.json` and the current plan from `runtime/plans/` to orient.
2. Update `runtime/ROADMAP.md` and the current plan if they have drifted.
3. Validate the current plan against the existing codebase.
4. Implement the plan.
5. Validate the implementation against the plan.
6. Run lint, typecheck, and build.
7. Update tests and run them.
8. Write a log entry to `runtime/log/`, update `runtime/state.json`, and continue.

## Rules

- Do not start implementation before the plan matches the current codebase.
- Do not call work complete until validation and tests pass.
- Update the current plan in `runtime/plans/` after every meaningful change.
- Write a `runtime/log/` entry for each completed loop iteration.
