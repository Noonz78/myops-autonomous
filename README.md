# Autonomous Workspace Foundation - myops-autonomous

## ⚠️ Current Status: Incomplete Configuration

This repository provides the **foundation** for autonomous work, but requires additional setup before OpenSpec and Superpowers are fully functional.

- ✅ Git repo initialized with full structure
- ✅ Task management commands ready (`/todo`, `/status`, `/loop`)
- ✅ Memory system configured at `.claude/memory/`
- ❌ **OpenSpec GitHub repo NOT cloned yet** (https://github.com/Fission-AI/OpenSpec)
- ❌ **Superpowers GitHub repo NOT cloned yet** (https://github.com/obra/superpowers)

## Getting Started

### Step 1: Clone Required Repositories

```bash
cd "D:\Repos\myops-autonomous"

# Clone OpenSpec
git clone https://github.com/Fission-AI/OpenSpec.git agents/openspec

# Clone Superpowers  
git clone https://github.com/obra/superpowers.git agents/superpowers
```

### Step 2: Configure for Full Functionality

Update `.claude/settings.json` to integrate the cloned repos as external tools. See `CLAUDE.md` for configuration instructions.

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
├── agents/superpowers/  # Superpowers repo (to be cloned)
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

### Run Autonomous Work (after cloning repos)
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
