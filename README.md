# Agent Epics — Curated Epic Collection

Public curated Epic source repositories authored by the [Agent Epics](https://agentepics.io) project.

Each directory is a complete Epic following the [EPIC specification v0.5.2](https://agentepics.io/epic-specification), containing a dual-purpose `SKILL.md`, `EPIC.md`, and durable runtime state under `runtime/`.

## Epics

| Epic | Category | Description |
|------|----------|-------------|
| [agent-heartbeat](agent-heartbeat/) | Automation | Wake an agent on a regular interval |
| [approval-management](approval-management/) | Governance | Track approval policy for autonomous work |
| [autonomous-coding](autonomous-coding/) | Execution | Run a robust coding loop with validation |
| [autonomous-planning](autonomous-planning/) | Planning | Daily planning loop for Epic portfolio health |
| [proactive-reporting](proactive-reporting/) | Communication | Disciplined reporting on schedule |
| [telegram-integration](telegram-integration/) | Communication | Telegram channel for questions and reports |

## Structure

Each epic follows the standard layout:

```
epic-name/
├── SKILL.md              # Skill surface plus Agent Epics footer
├── EPIC.md               # Workflow definition with YAML frontmatter
├── runtime/
│   ├── state.json        # Structured state
│   ├── plans/
│   │   └── 001-initial.md # Initial tactical plan
│   └── log/              # Append-only activity history
└── policy.yml
```

## License

Apache 2.0. See individual epics for details.
