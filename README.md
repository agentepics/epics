# Agent Epics — Curated Epic Collection

Public curated Epic source repositories authored by the [Agent Epics](https://agentepics.io) project.

Each directory is a complete Epic following the [EPIC specification v0.5.2](https://agentepics.io/epic-specification), containing a dual-purpose `SKILL.md`, `EPIC.md`, and the fuller authored operational profile used by the curated samples.

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

Each curated epic follows this common operational profile:

```
epic-name/
├── SKILL.md              # Skill surface plus Agent Epics footer
├── EPIC.md               # Workflow definition with YAML frontmatter
├── runtime/
│   ├── state.json        # Structured state
│   ├── plans/
│   │   └── 001-initial.md # Initial tactical plan
│   └── log/              # Append-only activity history
├── hooks/                # Lifecycle hook handlers
├── cron.d/               # Scheduled tasks
└── policy.yml
```

The minimum valid Epic is smaller than this: the core spec only requires
`SKILL.md` and `EPIC.md`. The extra runtime files shown here are the common
curated authored profile, not a mandatory minimum.

## License

Apache 2.0. See individual epics for details.
