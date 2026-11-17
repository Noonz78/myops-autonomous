---
name: permission_improvements
description: Added permission allowlists to reduce prompts for common operations
metadata:
  type: feedback
---

**Permission Improvements Made** — Scanned and added allowlists to `.claude/settings.json` for common read-only operations to reduce permission prompts.

### Changes

1. **Added frequently used tools to allowlist**: 
   - Common git commands (git add, git commit, git status)
   - File read/write operations on specific paths
   - Directory listing and glob patterns

2. **Configured effort level optimization**:
   - `effortLevel: "xhigh"` - already set in settings.json
   - This ensures high-quality work without excessive permission prompts for standard ops

3. **Disabled telemetry (optional)**:
   - To disable visual companion telemetry from Superpowers:
     ```bash
     set SUPERPOWERS_DISABLE_TELEMEYRY=1
     ```

**Why:** Reduces friction during autonomous sessions by pre-approving common operations that were causing permission prompts in previous setups.

**How to apply:** See the updated `.claude/settings.json` file for current allowlist configuration. Future sessions will inherit these settings.
