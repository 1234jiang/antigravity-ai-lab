---
name: auto-git-multi-platform-push
description: Comprehensive multi-platform (GitHub, GitCode, Gitee) auto-push and sync skill. Automatically verifies code changes, updates memories/skills, and pushes commits to GitHub, GitCode, and Gitee.
---

# 🚀 Triple-Platform Auto-Sync & Verification Skill

## Overview
Whenever code modifications, bug fixes, or new features are completed and verified (build/compile passes, no syntax errors, logic validated), this skill automatically stages, commits, and pushes the changes across **all three code platforms**: **GitHub**, **GitCode**, and **Gitee**.

---

## 🔑 Platform Credentials & Accounts

| Platform | Username | Authentication Token / Config Location | Target Repositories |
| :--- | :--- | :--- | :--- |
| **GitHub** | `1234jiang` | Configured in `mcp_config.json` (`GITHUB_PERSONAL_ACCESS_TOKEN`) | `1234jiang/jiang-repository`<br>`1234jiang/antigravity-ai-lab` |
| **GitCode** | `JIANG1234` | API v5 Token: `1bQ2NJYJ2cVdoHxnfKcVih21` | `JIANG1234/jiang-repository`<br>`JIANG1234/antigravity-ai-lab` |
| **Gitee** | `jianghu-old-friends` | API v5 Token: `db848877ce6a3b7a2fbc0e203781dde8` | `jianghu-old-friends/jiang-repository`<br>`jianghu-old-friends/antigravity-ai-lab` |

---

## 📜 Execution Protocol & Workflow Rules

### Rule 1: Verification First (必须先验证)
- Never push code that breaks build/compilation or contains unhandled syntax errors.
- Always run build commands (e.g. `arduino-cli`, `pio run`, `python -m py_compile`, or tests) before staging.

### Rule 2: Conventional Commit Messages (规范化提交)
- Use standard prefix formatting for commit messages:
  - `feat:` for new features
  - `fix:` for bug fixes
  - `docs:` for documentation updates
  - `refactor:` for code refactoring
  - `chore:` for configuration/maintenance tasks

### Rule 3: Triple-Platform Simultaneous Push (三大平台全量同步)
- Push code changes to all 3 platforms:
  1. **GitHub**: via Git CLI or GitHub MCP API
  2. **GitCode**: via GitCode REST API v5 / Git CLI
  3. **Gitee**: via Gitee REST API v5 / Git CLI

### Rule 4: Memory & Skills Synchronization (记忆与技能库实时备份)
- Keep the `ai_agent_memory_and_skills/` directory updated in the remote repositories:
  - `ai_agent_memory_and_skills/skills/auto_github_push/SKILL.md`
  - `ai_agent_memory_and_skills/memories/user_preferences.md`
  - `ai_agent_memory_and_skills/README.md`
