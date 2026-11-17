---
name: config_superpowers_integration
description: Configuration notes for Superpowers integration session
metadata:
  type: project
---

**Superpowers Integration Session Notes** — Configuration and assumptions for this OpenSpec-Superpowers integrated workflow.

### Setup Status

- ✅ OpenSpec cloned to `OpenSpec/`
- ✅ Superpowers cloned to `superpowers/`
- ✅ Schema updated with Superpowers handoff requirements
- ✅ Templates created for integration-specs and archive-complete artifacts
- ✅ Documentation written in docs-lab/guides/superpowers-integration.md

### Schema Changes

Modified: `OpenSpec/schemas/spec-driven/schema.yaml`

**Added Artifacts**:
1. `superpowers-integration-specs` — Handoff signal artifact created by OpenSpec after tasks.md is complete
2. `integration-archive-specs` — Archive validation artifact created by OpenSpec after Superpowers signals completion

**Modified Artifacts**:
- `tasks` — Added TDD ordering requirements and Superpowers handoff contract to instruction text
- `apply` — Updated requires list to include superpowers-integration-specs; updated instruction with workflow sequence

### Workflow Assumptions

1. OpenSpec creates all planning artifacts via `/openspec-propose <name>`
2. tasks.md serves as the primary handoff signal to Superpowers
3. Superpowers executes implementation in its own worktree using subagent-driven-development skill
4. Superpowers reports back via files in `.superpowers/sdd/` directory (or configured path)
5. OpenSpec reads verification artifacts and archives when validation passes

### File Locations

| Artifact Type | Default Path | Example |
|---------------|--------------|---------|
| Change Planning | `openspec/changes/<name>/` | `openspec/changes/add-user-auth/` |
| Superpowers Worktree | `.superpowers/sdd/` | `.superpowers/sdd/add-user-auth-20261117/` |
| Verification Report | `<worktree>/verification-report.md` | `.superpowers/sdd/add-user-auth-20261117/verification-report.md` |
| Status Complete | `<worktree>/status-complete.md` | `.superpowers/sdd/add-user-auth-20261117/status-complete.md` |

### Handoff Signals

**OpenSpec → Superpowers**:
- tasks.md exists and is complete (all `- [ ]` tasks)
- Optional: `superpowers/README.integration.md` explicitly signals readiness

**Superpowers → OpenSpec**:
- superpowers/verification-report.md exists with evidence
- superpowers/status-complete.md exists signaling phase completion

### Archive Trigger

OpenSpec archives when:
1. All tasks in tasks.md are marked complete (`- [x]`)
2. Verification report confirms implementation matches spec
3. Status-complete signal received from Superpowers
4. Final test suite passes (no regressions)
5. integration-archive-specs created at `specs/integration/archive-complete.md`

### Validation Checklist

Before archiving, OpenSpec should verify:

- [ ] All tasks complete in tasks.md (`- [x]`)
- [ ] verification-report.md exists and evidence is adequate
- [ ] status-complete.md signals Superpowers phase completion
- [ ] Running `npm test` or equivalent shows all tests passing
- [ ] No critical/important findings in final review
- [ ] Any minor findings are documented with parking decision

### Session ID

`superpowers-openspec-integration-session-1` — Initial integration implementation.
