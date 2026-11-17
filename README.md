# Autonomous Workspace Foundation - myops-autonomous

## ✅ Current Status: Configured

This repository provides the foundation for autonomous work with OpenSpec and Superpowers **already integrated**.

- ✅ Git repo initialized with full structure
- ✅ Task management commands ready (`/todo`, `/status`, `/loop`)
- ✅ Memory system configured at `.claude/memory/`
- ✅ **OpenSpec GitHub repo cloned** (https://github.com/Fission-AI/OpenSpec)
- ✅ **Superpowers GitHub repo cloned** (https://github.com/obra/superpowers)

## Quick Start

```bash
cd "D:\Repos\myops-autonomous"

# Optional: Install OpenSpec CLI for command-line skills
irm https://openspec.dev/cli/install.ps1 | iex

# Register Superpowers plugin (optional but recommended)
/plugin install superpowers@superpowers-marketplace
```

See `CLAUDE.md` for full documentation and next steps.

## Features (Available After Setup)

- **OpenSpec Integration**: Auto-generates specs and docs as you code
- **Task Management**: Create, track, and complete tasks automatically
- **Agent Superpowers**: Multi-step autonomous task execution
- **Persistent Memory**: Knowledge persists across sessions

## Commands

| Command | Purpose |
|---------|---------|
| `/todo <subject>` | Create a new task |
| `/loop [interval] /prompt` | Run autonomous iterative work |
| `/status` | Check task status |
| `/plan` | Open plan mode for complex tasks |

## Project Structure

```
myops-autonomous/
├── .claude/              # Session state, plans, memory
│   ├── memory/          # Persistent knowledge base
│   ├── settings.local.json
│   └── scratch/         # Temp files (STARTUP-PROMPT.md)
├── OpenSpec/            # Cloned OpenSpec repo
├── superpowers/         # Cloned Superpowers repo
├── docs/specs/          # Auto-generated OpenSpec output
├── tasks/               # Task queue and progress
├── .scratch/            # Startup prompts, temp files
└── README.md            # This file
```

## Quick Reference

### Create a Task
```bash
/todo Add user authentication flow
```

### Run Autonomous Work

```bash
# Run every 10 minutes
/loop 10m /status
```

### View Configuration Status

See `.scratch/STARTUP-PROMPT.md` for:
- Current configuration status
- What needs to be done next
- Template prompt for new sessions

## See Also

- `CLAUDE.md` - Full documentation with detailed commands
- `.scratch/STARTUP-PROMPT.md` - Startup prompt template for new sessions
