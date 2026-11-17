# Autonomous Work Repo

This is an autonomous workspace designed for self-driving development with OpenSpec integration.

## Architecture

```
├── .claude/                    # Session state & configs
│   ├── plans/                  # Multi-step task plans
│   ├── memory/                 # Long-term knowledge
│   └── plugins/               # MCP server integrations
├── docs/                       # Auto-generated documentation
│   ├── specs/                 # OpenSpec models
│   ├── runbooks/             # Operational procedures
│   └── architecture/        # System designs
├── tasks/                      # Task definitions & progress
│   ├── active/               # Currently working on
│   ├── backlog/              # Queue of pending work
│   └── completed/           # Finished work
├── agents/                    # Agent configurations
│   └── superpowers/         # Extended agent capabilities
└── outputs/                   # Generated artifacts
```

## Capabilities

### OpenSpec Integration
- Auto-generate specs from code changes
- Maintain living documentation that stays in sync
- Extract models, protocols, and workflows automatically

### Agent Superpowers
- Multi-step task execution with state persistence
- Autonomous research across web/codebase
- Cross-file consistency checks
- Context-aware refactoring decisions

### Task Management
- Create/resolve structured todo lists
- Track progress with dependency graphs
- Auto-generate commit messages from work done

## Quick Start

```bash
# Initialize workspace
git init
git add .
git commit -m "Initial autonomous setup"

# Run your first autonomous task
/claire start  # or /loop for iterative work
```
