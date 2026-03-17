---
title: "Tip #18: Commit before you let the agent loose"
date: 2026-03-14
categories: ["Workflow Patterns"]
weight: 18
summary: ""
---

A habit that pays for itself immediately: **commit (or stash) before asking the agent to make changes.**

AI agents touch multiple files at once. Without a clean baseline, it's hard to tell what the agent changed vs. what was already there — and harder to undo just the parts you don't want.

With a checkpoint:
1. `git commit -m "checkpoint"` (or `git stash`)
2. Let the agent work
3. `git diff` to see exactly what changed
4. Keep what's good, `git checkout -- <file>` to revert what isn't

This is especially valuable for agentic workflows (Copilot CLI, Claude Code, Cursor) where the agent runs multiple steps autonomously. In chat-based workflows you review inline diffs, but in agent mode it might edit five files before you look.

I'm a fan of small commits — even micro-commits. Getting AI agents to commit that granularly is still hard, but at least make sure _you_ commit before handing over control. That way the agent's changes are always one `git diff` away from a clean state.

Save your game before the boss fight.

💡 Try this: Before your next AI-assisted change, run `git stash` or make a quick commit. After the agent finishes, run `git diff` and review the changes as if they came from a colleague's PR.

🔗 [Review AI-generated code edits (VS Code docs)](https://code.visualstudio.com/docs/copilot/chat/review-code-edits)

_Do you create a checkpoint before AI-assisted changes?_  

---

🟢 Always — commit or stash first  
🟡 Sometimes, when it's a big change  
🔴 No — I rely on undo / inline diffs  
⚪ I mostly use chat, not agent mode

_Any git tricks that work well with AI workflows? Share in 🧵_