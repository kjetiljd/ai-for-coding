---
title: "Tip #22: Use scripts for repeatable tasks"
date: 2026-03-18
categories: ["Workflow Patterns"]
weight: 22
summary: "Deterministic tasks deserve deterministic scripts — not AI improvisation every session."
description: "Deterministic tasks deserve deterministic scripts — not AI improvisation every session."
---

*AI agents are great at figuring things out — but some tasks shouldn't require figuring out. Restarting services, resetting test data, deploying a build — these should work the same way every time.*

When something is deterministic, make it a script. Don't let the agent improvise what should be repeatable. A script gives you the same result every run, costs zero tokens to execute, and removes a whole class of "the agent did something slightly different this time" surprises.

"Script" is broad here — a bash script, a Makefile target, an `npm run` command, a Gradle task. You can use whatever your ecosystem already has. Agents already know how to call `make`, `npm run`, and `./gradlew` — using familiar tools means less explaining.

Every step the agent re-solves from scratch is a step that can drift. `npm run reset-dev` doesn't drift.

💡 Try this: Think of one multi-step task you keep describing to the agent. Make it a script instead — then tell the agent to use that.

---

**How do you handle repeatable tasks with your agent?**

🟢 Scripts and Makefiles — the agent runs them  
🟡 I have some scripts, but the agent doesn't use them  
🔴 I mostly just explain it to the agent each time  
⚪ Haven't thought about it

*What's a task you've scripted (or should script)?*