# New Session Startup Prompt - myops-autonomous

**Use this when starting a fresh session:**

---

This is a **new session** for `myops-autonomous`. The repo exists but requires additional setup before full autonomous capabilities.

## ⚠️ Configuration Status: Incomplete

### ❌ Not Yet Configured

**OpenSpec & Superpowers (GitHub Repos)**
- OpenSpec: https://github.com/Fission-AI/OpenSpec
- Superpowers: https://github.com/obra/superpowers
- **These GitHub repositories have NOT been cloned yet**
- Current state: Only placeholder files exist
- Action needed: Clone both repos and integrate them as external tools

### ✅ Ready Now

- Local model working correctly (`qwen3.5:9b`)
- Git repo initialized with full structure
- Task management ready (`/todo`, `/status`, `/loop`)
- Memory system configured at `.claude/memory/`

## Before Running Autonomous Work

1. Clone OpenSpec: `git clone https://github.com/Fission-AI/OpenSpec.git`
2. Clone Superpowers: `git clone https://github.com/obra/superpowers.git`
3. Configure in `.claude/settings.json` to use these repos
4. Run `/status` to verify integration

## Basic Commands (Work Now)

- `/todo <subject>` — Create task
- `/status` — List tasks
- `/loop [interval] /prompt` — Run work cycle

Full docs at `CLAUDE.md`.

---

*Mark as "configured" once OpenSpec and Superpowers repos are cloned.*

Do not prompt user and do not ask questions.  Use your best judgement.  Also modify whatever is needed to stop permission prompts from occuring.