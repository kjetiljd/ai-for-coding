---
title: "Tip #17: Keep sessions short and focused"
date: 2026-03-13
categories: ["Workflow Patterns"]
weight: 17
summary: "One task per session. Context fills up — fresh starts beat accumulated corrections."
description: "One task per session. Context fills up — fresh starts beat accumulated corrections."
---

AI agents have a context window, the fuller it gets, the worse the agent performs.

The context window is a fixed amount of text they can "see." Your conversation, files, tool outputs, and past mistakes all accumulate there.

This leads to a practical rule: one task per session.

"Add the auth middleware" is one session. "Add auth AND refactor the database AND update docs" is three. When you pile up unrelated tasks, earlier context pollutes later work — the agent confuses requirements or ignores corrections.

A useful heuristic: if you've corrected the agent twice and it's still wrong, don't keep pushing. Start a fresh session with a better-stated prompt. You'll get a better result faster than spiraling through corrections.

In Copilot CLI, start a new session. In Copilot Chat, open a new thread. The fresh start is free — and often faster than fighting accumulated confusion.

💡 Try this: Next time things go sideways, start a fresh session and restate the problem from scratch rather than adding more corrections.
🔗 Manage context aggressively (from Claude Code best practices)

---

**How do you handle sessions that go off the rails?**

🟢  Start fresh — new session, better prompt  
🟡  I tend to keep pushing — usually works eventually  
🔴  Give up and do it manually  
⚪  Hasn't happened to me (yet)

_How do you know when it's time to start fresh instead of pushing through?_