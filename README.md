# Autonomous Workspace with OpenSpec Integration

This repo is configured for self-driving development work with automatic documentation.

## Features

- **OpenSpec Integration**: Auto-generates specs and docs as you code
- **Task Management**: Create, track, and complete tasks automatically
- **Agent Superpowers**: Multi-step autonomous task execution
- **Persistent Memory**: Knowledge persists across sessions

## Getting Started

```bash
cd "D:\Repos\myops-autonomous"
git add .
git commit -m "Initial setup with OpenSpec and agents"
```

## Commands

| Command | Purpose |
|---------|---------|
| `/todo <subject>` | Create a new task |
| `/loop [interval] /prompt` | Run autonomous iterative work |
| `/status` | Check task status |
| `/plan <task>` | Open plan mode for complex tasks |

## Project Structure

```
myops-autonomous/
├── .claude/              # Session state, plans, memory
│   ├── memory/          # Persistent knowledge base
│   ├── plans/           # Multi-step task plans
│   └── settings.local.json
├── agents/superpowers/  # Agent configurations
├── docs/specs/          # Auto-generated OpenSpec docs
├── tasks/               # Task queue and progress
└── README.md            # This file
```

## How to Use

### Create a Task
```
/todo Add user authentication flow
```

### Run Autonomous Work
```
/loop 10m /status
```
This runs `/status` every 10 minutes, checking tasks and working autonomously.

### Plan Complex Implementation
```
/openplan - Enter plan mode before starting major features
```

## OpenSpec Integration

OpenSpec automatically generates documentation:
- Extract API specs from code changes
- Generate model diagrams from data structures
- Create runbooks for operational procedures
- Maintain architecture docs that stay in sync

See `docs/specs/` for generated content.
