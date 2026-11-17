---
name: superpowers-openspec-integration
description: OpenSpec → Superpowers → OpenSpec handoff workflow implemented
metadata:
  type: project
---

**Superpowers-OpenSpec Integration Complete** — Integrated Superpowers' specification-driven development (SDD) with OpenSpec's change proposal and archiving system.

### Workflow Sequence

1. **OpenSpec propose** → Creates all planning artifacts (proposal, specs, design, tasks.md)
2. **Handoff to Superpowers** → Create `superpowers/README.integration.md` to signal readiness
3. **Superpowers SDD execution** → TDD implementation per tasks.md:
   - Write failing test first (RED)
   - Verify test fails correctly
   - Implement minimal code (GREEN)
   - Commit changes
   - Repeat for each task
4. **Verification handoff** → Superpowers creates:
   - `superpowers/verification-report.md` with completion evidence
   - `superpowers/status-complete.md` to signal phase completion
5. **OpenSpec archive validation** → OpenSpec:
   - Reads verification report
   - Runs final test suite
   - Creates `specs/integration/archive-complete.md`
   - Archives the change

### Required Artifacts by Phase

#### OpenSpec creates (for Superpowers)
- proposal.md — The why
- specs/**/*.md — Behavior contracts with scenarios
- design.md — Technical approach (when needed)
- tasks.md — TDD-ordered implementation checklist (handoff signal)
- superpowers/README.integration.md — Handoff signal

#### Superpowers creates (for OpenSpec validation)
- superpowers/verification-report.md — Evidence of completed work with test results
- superpowers/status-complete.md — Phase completion signal

### Template Files Created

- `OpenSpec/schemas/spec-driven/templates/integration-specs.md` — Superpowers handoff template
- `OpenSpec/schemas/spec-driven/templates/archive-complete.md` — Archive validation template

### Documentation

- `OpenSpec/docs-lab/guides/superpowers-integration.md` — Complete workflow guide

### Key Design Decisions

1. **TDD is mandatory** — Code before failing test is deleted per Superpowers discipline
2. **Tasks are the handoff signal** — tasks.md with complete checkbox list signals implementation readiness
3. **Verification reports are required** — OpenSpec validates against evidence in verification-report.md
4. **Minimal viable code only** — YAGNI principle; over-engineering is a defect

### See Also

- .claude/memory/config_superpowers_integration.md — Session configuration notes
- OpenSpec/schemas/spec-driven/schema.yaml — Updated workflow schema
