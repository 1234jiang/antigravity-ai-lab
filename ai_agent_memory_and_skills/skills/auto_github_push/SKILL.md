---
name: auto-github-push
description: Auto-push code changes to GitHub repository after verification. Triggers when code edits or bug fixes are verified and ready.
---

# Auto GitHub Push Skill

## Overview
When code modifications or bug fixes are completed and verified (tests pass, build succeeds, or manually confirmed working), automatically stage, commit, and push the changes to the user's GitHub repository.

## Rules & Protocol
1. **Verification First**:
   - Ensure the modified code builds, compiles, or passes validation before pushing.
   - Never push code that breaks compilation or fails runtime checks.

2. **Commit & Push Procedure**:
   - Use descriptive commit messages clearly summarizing the changes made (e.g., eat: ..., ix: ..., efactor: ...).
   - Push either via Git CLI (git add ., git commit -m "...", git push) or via GitHub MCP API (push_files / create_or_update_file).

3. **Target Repository**:
   - Current active workspace repository: 1234jiang/jiang-repository (or 1234jiang/antigravity-ai-lab).