---
title: "Tip #49: Master the handoff"
date: 2026-07-28
categories: ["Workflow Patterns"]
weight: 49
summary: "Handoffs happen constantly — compaction, subagents, fresh sessions — and the receiver can't ask what you meant. Record the why, not just the what, and hand off before you hit the wall, not after."
---

Every time work moves from one session to another — or from the main agent to a subagent, a fresh agent, or in real life from you to a teammate — that's a *handoff*. With AI coding agents handoffs happen often and sometimes invisibly: auto-compaction firing, work being given to a subagent — or you starting a fresh session (e.g. with `/clear`) after a plan or spec has been written.

The catch here: *the receiver can't ask the sender what it meant, so any handoff artifact has to stand on its own*. For example a good handoff should record not just the **what**, but also the **why**, otherwise the next session might reopen settled questions.

Here's a timing trick to try: don't wait for auto-compaction to rescue you — it fires when the context is nearly full, which is when the model is at its least sharp. Hand off **before** you hit the wall. When a session gets heavy, run `/compact focus on the schema decisions` to steer what survives.

An expert trick is to have a ready made instruction (or perhaps even a skill) that puts the handoff-information in a file you can review, and even bring from one coding agent to another (Running out of Claude Code-credits? Create a handoff doc and bring it into Copilot CLI).

Bonus: a fresh session with a good brief has no sunk-cost bias — it is not confused by dead ends and won't hold on to what a tired session kept defending.

💡 Try this: tell your agent: *"Write a handoff doc for a fresh session that knows nothing about this work."* (or try one of the skills below)

🔗 [Anthropic on session management](https://claude.com/blog/using-claude-code-session-management-and-1m-context)  
🔗 [Matt Pocock's lightweight /handoff skill](https://github.com/mattpocock/skills/blob/main/skills/productivity/handoff/SKILL.md)  
🔗 [ToolMonster's cross-agent handoff](https://github.com/ToolMonsters/handoff-skill/blob/main/SKILL.md)  
🔗 [Softaworks' Session Handoff](https://github.com/softaworks/agent-toolkit/blob/main/skills/session-handoff/SKILL.md)

---

**How do you carry context between sessions?**

🟢 I make sure I have reviewable handoff docs / compact deliberately  
🟡 I just start over and re-explain or let auto-compaction deal with it  
🔴 I often lose context and feel it  
⚪ Haven't hit this yet

_Got a handoff trick you like? Drop it in