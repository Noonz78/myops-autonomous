# Agent Task Prompts

## Autonomous Work Patterns

### Status Check Loop
```
Check task list for pending work
For each active task:
  - Verify prerequisites met
  - Execute relevant agents
  - Document progress
Mark completed tasks
Create follow-up tasks as needed
```

### Research Mode
```
1. Explore codebase to understand context
2. Gather requirements from docs/issues
3. Plan implementation approach
4. Get approval before implementing
5. Implement and verify
6. Write/update documentation
```

### Documentation Generation
When code changes:
1. Analyze what was changed
2. Update relevant specs
3. Generate diagrams if needed
4. Create runbook entries
5. Link to related docs
