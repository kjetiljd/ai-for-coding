---
title: "Tip #27: Subagents are now a standard pattern — here's what that means"
date: 2026-04-20
categories: ["Agents / Advanced Workflows"]
weight: 27
summary: "Subagents are fresh agents spawned for specific tasks with clean context windows. Every major coding agent now supports them — use them to avoid context rot and run explorations in parallel."
---

_Your agent has been exploring, editing, running tests — and now you're 40 messages in and the answers are getting vague. Context rot has set in._

**Subagents** fix this. A subagent is a fresh agent that the main agent spawns for a specific task. It gets its own context window — clean, focused, no history from the parent session. When it's done, only the result comes back. Your main context stays light.

Two reasons this is a game-changer:
— **Context doesn't fill up.** A subagent exploring 15 files doesn't pollute the parent's context with all 15. The parent only sees the summary.
— **Parallelism.** You can run multiple subagents at once — one exploring the backend, one checking the frontend, one running tests. They work simultaneously.

Every major coding agent now supports this: Copilot CLI, Claude Code, Codex, Cursor, OpenCode. The pattern has converged. In Copilot CLI, it's the `task` tool. In Claude Code, the `Task` tool with `mode: "background"`.

If you've been following tips [#16](/tips/016-explore-before-you-edit/) and [#17](/tips/017-short-focused-sessions/) — subagents are the automated version of both.

💡 Try asking for a subagent next time you have a concrete subtask: "use a subagent to find all the places we handle authentication errors."
🔗 [VS Code Copilot subagents docs](https://code.visualstudio.com/docs/copilot/agents/subagents)

---

**Have you used subagents / the task tool?**

🟢 Yes — I delegate regularly  
🟡 Tried it once or twice  
🔴 Didn't know my agent could do this  
⚪ I prefer doing everything in one session

_What would you delegate to a subagent?_