# Agent Epics — Curated Epic Collection

Public curated Epic source repositories authored by the [Agent Epics](https://agentepics.io) project.

Each directory is a complete Epic following the [EPIC specification v0.5.0](https://agentepics.io/epic-specification), containing `SKILL.md`, `EPIC.md`, structured state, plans, and log directories.

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
├── SKILL.md              # Routing and instructions
├── EPIC.md               # Workflow definition with YAML frontmatter
├── state.json            # Structured state
├── plans/
│   └── 001-initial.md    # Initial tactical plan
└── log/                  # Append-only activity history
```

## License

Apache 2.0. See individual epics for details.
