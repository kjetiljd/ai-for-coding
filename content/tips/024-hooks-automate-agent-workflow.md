---
title: "Tip #24: Automate the boring parts with hooks"
date: 2026-04-16
categories: ["Workflow Patterns"]
weight: 24
summary: "Hooks are shell commands that fire automatically at agent lifecycle points — before/after a tool runs, on session start, on finish. Unlike instruction files, they're deterministic. Enforce your venv rule, run tests after edits, get a desktop notification when the agent is done."
---

_Your instruction file says "always use the virtual environment for Python." The agent reads it, nods, and then calls bare `python3` anyway. Sound familiar?_

That's where **hooks** come in. Hooks are shell commands that fire automatically at specific points in the agent's workflow — before or after a tool runs, when a session starts, when it finishes. Unlike instruction files (which are advisory), a hook **always** runs.

Three useful examples:
— `preToolUse`: block bare `python3` calls that skip the venv — the agent gets a clear error message instead of a silent wrong environment
— `postToolUse`: run your test suite after every file edit — Claude Code lets you target `Edit|Write` tools specifically with a matcher; Copilot CLI fires on all tools so your script filters by `toolName`
— `Stop` / `Notification`: get a macOS desktop notification when the agent finishes or needs input — useful when you've wandered off to do something else (see: CCNotify)

Both Copilot CLI and Claude Code support hooks. The naming differs slightly, but the concept is the same: a trigger point, a shell command, done.

💡 Try this: pick one thing your agent keeps forgetting or that you keep doing manually — and hook it.
🔗 [Using hooks with Copilot CLI](https://docs.github.com/en/copilot/how-tos/copilot-cli/customize-copilot/use-hooks)  
🔗 [CCNotify — desktop notifications for Claude Code](https://github.com/dazuiba/CCNotify)

---

**Do you use hooks or automated checks with your coding agent?**

🟢 Yes — I've automated something  
🟡 Not yet, but I want to  
🔴 Still doing it manually  
⚪ Didn't know this was possible

_What would you automate with a hook?_