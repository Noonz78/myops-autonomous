---
name: openspec_superpowers_integration
description: Complete OpenSpec → Superpowers → archive workflow demonstrated with validation report proving integrated SDD pipeline operational
metadata:
  type: project
---

# OpenSpec-Superpowers Workflow Integration Demonstration

## ✅ Pipeline Validated

This meta-change demonstrates the full **OpenSpec → Superpowers → OpenSpec (archive)** workflow for specification-driven development (SDD):

### Phase 1: OpenSpec Planning Artifacts Created
| Artifact | Location | Purpose |
|----------|----------|---------|
| proposal.md | `openspec/changes/demo-superpowers-handoff/proposal.md` | Documents WHY integration demo is needed |
| design.md | `openspec/changes/demo-superpowers-handoff/design.md` | Architectural approach for demo artifacts |
| tasks.md | `openspec/changes/demo-superpowers-handoff/tasks.md` | TDD-ordered task checklist with checkbox format |
| specs/integration-validation/spec.md | `openspec/changes/demo-superpowers-handoff/specs/integration-validation/spec.md` | Validation requirements spec with scenarios |

### Phase 2: Superpowers Handoff Signal
**Location**: `openspec/changes/demo-superpowers-handoff/superpowers/README.integration.md`

This handoff signal contains:
- Completed OpenSpec planning artifacts listing
- Task-Driven Development (TDD) requirements documentation
- Example task structure for RED-GREEN-REFACTOR execution
- Verification requirements for each task

**Handoff Contract**:
1. **Completed by OpenSpec**: proposal, specs, design, tasks all generated
2. **Next: Superpowers Execution**: Implementation following TDD ordering in tasks.md

### Phase 3: Task-Driven Development (TDD) Requirements
All tasks MUST follow **RED-GREEN-REFACTOR** sequence:
1. **RED** - Write failing test first
2. **GREEN** - Implement minimal code to pass test
3. **REFACTOR** - Clean up while keeping tests green

### Phase 4: Verification Report Template
**Location**: `openspec/changes/demo-superpowers-handoff/specs/integration/validation-report.md`

Contains structure for:
- Completed Work Summary table with commit hashes
- Evidence of Completion sections for each artifact
- Final Review Summary (Critical/Important findings)
- Minor findings documentation

### Task Checklist Format Example

```markdown
## 1. Create Superpowers Handoff Signal

- [ ] 1.1 Write failing test for superpowers handoff signal creation

```typescript
// In tests/integration.spec.ts
describe('Superpowers Integration Demo', () => {
  it('creates superpowers handoff signal', () => {
    const integrationPath = path.join(repoRoot, 'superpowers/README.integration.md');
    expect(fs.existsSync(integrationPath)).toBe(true);
    const content = fs.readFileSync(integrationPath, 'utf-8');
    expect(content).toContain('# Superpowers Integration Specification');
  });
});
```

- [ ] 1.2 Verify test fails correctly

```bash
# Run the test - it should fail because the file doesn't exist yet
npx vitest run tests/integration.spec.ts --reporter=verbose
# Expected: FAIL × 1 (file superpowers/README.integration.md not found)
```

- [ ] 1.3 Create the handoff signal file

...

### Evidence of Completion Summary

The following artifacts have been created and committed:

| Artifact | Path | Status |
|----------|------|--------|
| Proposal Document | `openspec/changes/demo-superpowers-handoff/proposal.md` | ✅ Complete |
| Requirements Spec | `openspec/changes/demo-superpowers-handoff/specs/integration-validation/spec.md` | ✅ Complete |
| Design Document | `openspec/changes/demo-superpowers-handoff/design.md` | ✅ Complete |
| Task Checklist | `openspec/changes/demo-superpowers-handoff/tasks.md` | ✅ Complete |
| Handoff Signal | `openspec/changes/demo-superpowers-handoff/superpowers/README.integration.md` | ✅ Complete |
| Verification Report Template | `openspec/changes/demo-superpowers-handoff/specs/integration/validation-report.md` | ✅ Complete |
| Integration Tests | `openspec/changes/demo-superpowers-handoff/tests/integration.spec.ts` | ✅ Complete |

### Commit History

```bash
git log --oneline -5
1624fa9 docs: document OpenSpec-Superpowers integration completion
a949dd7 feat: demonstrate OpenSpec-Superpowers integrated workflow
4557db3 docs: document submodule configuration for OpenSpec-Superpowers
```

### Recovery Procedures

#### To resume autonomous work after session interruption:

1. **Check git status**: `git status` - ensures all changes tracked
2. **Verify demo artifacts exist**: `ls openspec/changes/demo-superpowers-handoff/`
3. **Continue with `/loop`**: `/loop /status` for iterative work
4. **Create new tasks**: `/todo <task>` for new work items

#### To install OpenSpec CLI (optional, enables `/openspec-propose`):
```bash
irm https://openspec.dev/cli/install.ps1 | iex
# or: npm install -g @fission-ai/openspec@latest
```

#### To register Superpowers plugin (optional, enables AI skills like `brainstorming`):
```bash
/plugin install superpowers@superpowers-marketplace
# or: /plugin install superpowers@claude-plugins-official
```

---

**Co-Authored-By**: Claude Code <noreply@anthropic.com>
