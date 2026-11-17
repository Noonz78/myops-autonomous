# Autonomous Work Repo - myops-autonomous

This repository is configured for self-driving development with OpenSpec integration and agent superpowers.

## Overview

- **Model**: Using local qwen3.5:9b for autonomous execution
- **Goal**: Self-driving work with automatic documentation generation
- **Mode**: xhigh effort level with persistent session state

## Project Structure

```
myops-autonomous/
├── .claude/                    # Session configs & memory
│   ├── settings.json          # Project-specific config
│   ├── memory/                # Persistent knowledge base
│   ├── plans/                 # Multi-step task plans
│   └── tasks/                 # Task queue (active, backlog, completed)
├── agents/                     # Agent configurations
│   └── superpowers/           # Extended capabilities
├── docs/                       # Auto-generated documentation
│   └── specs/                 # OpenSpec generated content
├── tasks/                      # Task definitions
└── README.md                   # This guide
```

## Commands Guide

### Task Management

| Command | Purpose |
|---------|---------|
| `/todo <subject>` | Create new task |
| `/status` | List all tasks |
| `/task <id> complete` | Mark task done |
| `/loop [interval] /prompt` | Run iterative work loop |

### Planning Mode

- `/plan` - Enter plan mode for complex tasks
- Exit with `ExitPlanMode` when ready
- Review and approve plan before implementation

### Agent Commands

- `/agent <name> <description>` - Spawn specialized agent
  - `claude` - General purpose, all tools
  - `plan` - Architecture decisions (read-only)
  - `explore` - Code search with glob/grep
  - `general-purpose` - Complex multi-step work

## OpenSpec Integration

OpenSpec auto-generates documentation as you work:

```json
docs/specs/open-spec-manifest.json  // Auto-generated specs
docs/runbooks/                       // Operational procedures
docs/architecture/                   // System designs
```

### Triggered by:
- Code changes in your project
- Task completion summaries
- Architecture modifications

## Agent Superpowers

Enabled capabilities:

1. **Autonomous Execution**
   - Tasks persist across sessions
   - Progress tracked in task files
   - Dependencies auto-resolved

2. **Cross-File Context**
   - Understand relationships between files
   - Make consistent refactoring decisions
   - Know what to change and why

3. **Self-Pacing**
   - Agents run at optimal intervals
   - Long tasks use background mode
   - Fall back heartbeats for stuck work

4. **Research & Exploration**
   - Web search for external context
   - Codebase grep/search operations
   - Pattern matching across files

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

### Running Autonomous Work
```bash
# Check status and continue working
/status

# Run iterative loop (checks every 10 min)
/loop 10m /status
```

## Memory System

Knowledge persists in `.claude/memory/`:
- `user.md` - Your role and preferences
- `feedback.md` - How to work with you
- `project.md` - Current project context
- `reference.md` - External resource links

See `MEMORY.md` for the full index.

## Settings

Located at `.claude/settings.json`:
- `model`: qwen3.5:9b (local)
- `effortLevel`: xhigh (thorough work)
- `autonomousMode`: true
- `openSpecIntegration.enabled`: true

## Tips

1. **Create tasks before working** - Lets agents track progress
2. **Use `/loop` for long sessions** - Keeps work autonomous
3. **Exit plan mode after review** - Triggers implementation
4. **Check memory grows organically** - Documents what you've learned
5. **Review generated specs periodically** - Verify OpenSpec accuracy
