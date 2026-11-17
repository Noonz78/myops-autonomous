# Autonomous Work Repo - myops-autonomous

This repository provides the foundation for self-driving development with OpenSpec and Superpowers integration.

## ⚠️ Important: Incomplete Setup

**This repo is ready but NOT fully configured yet.** The GitHub repositories for OpenSpec and Superpowers need to be cloned before full autonomous capabilities work.

See `.scratch/STARTUP-PROMPT.md` for the startup prompt template that new sessions should use.

## Overview

- **Model**: Using local qwen3.5:9b for autonomous execution
- **Goal**: Self-driving work with automatic documentation generation
- **Mode**: xhigh effort level with persistent session state

## Project Structure

```
myops-autonomous/
├── .claude/                    # Session configs & memory
│   ├── settings.json          # Project-specific config
│   └── memory/                # Persistent knowledge base
├── agents/superpowers/        # Agent configurations (placeholder)
├── docs/specs/               # OpenSpec output location
├── tasks/                    # Task definitions & queue
├── .scratch/                 # Temp files, startup prompts
├── CLAUDE.md                 # This guide
└── README.md                 # Quick reference
```

## Commands Guide

### Task Management

| Command | Purpose |
|---------|---------|
| `/todo <subject>` | Create new task |
| `/status` | List all tasks |
| `/loop [interval] /prompt` | Run iterative work loop |

### Planning Mode

- `/plan` - Enter plan mode for complex tasks
- Exit with `ExitPlanMode` when ready
- Review and approve plan before implementation

## ⚠️ Before Using OpenSpec & Superpowers

These GitHub repositories must be cloned first:

1. **OpenSpec**: `git clone https://github.com/Fission-AI/OpenSpec.git`
2. **Superpowers**: `git clone https://github.com/obra/superpowers.git`

Then configure `.claude/settings.json` to use these as external tools.

## Getting Started

### First Time Setup (Already Done)

```bash
cd "D:\Repos\myops-autonomous"
git add .
git commit -m "Initial setup"
```

### Creating Your First Task

```bash
/todo Implement user authentication flow
/todo Set up CI/CD pipeline
/todo Write integration tests
```

### Running Autonomous Work (After Cloning Repos)

```bash
# Check status and continue working
/status

# Run iterative loop (checks every 10 min)
/loop 10m /status
```

## Scratch Files

Temporary files and startup prompts are stored in `.scratch/`:

- `STARTUP-PROMPT.md` - Template for starting a new session
- Shows configuration status and what needs to be done
- Copy this file when moving the repo or creating backups

## Tips

1. **Create tasks before working** - Lets agents track progress
2. **Use `/loop` for long sessions** - Keeps work autonomous
3. **Clone OpenSpec & Superpowers first** - Before using full autonomous features
4. **Check `.scratch/STARTUP-PROMPT.md`** - For accurate configuration status
