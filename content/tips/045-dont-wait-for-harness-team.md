---
title: "Tip #45: Don't wait for a \"harness engineering team\""
date: 2026-07-08
categories: ["Beyond Copilot / Reflective"]
weight: 45
summary: "Your agent = model + harness. Centralising the harness in a dedicated team likely repeats the DevOps-team mistake — the friction of each team building its own is where the learning happens."
---

Your agent = model + harness. The harness is everything wrapped around the model: your AGENTS.md, hooks, skills, MCP setup, the guidelines you add each time it messes up. As this scaffolding starts to matter more than model choice, some orgs are spinning up dedicated "harness engineering teams" to own it centrally.

That instinct probably repeats the DevOps-team mistake. "DevOps" was about tearing down the wall between dev and ops — so of course many orgs created a separate DevOps team and quietly rebuilt the wall.

A harness is shaped by *your* learning. The friction of a team building its own harness isn't waste to be centralised away; it's where the learning happens.

Share starting points and skills, yes. Hand ownership of your harness to another team, no.

💡 Try this: Open your team's AGENTS.md (or similar). Is every line traceable to something of value to you? If it's thin, add one rule from this week's mess ;-) — don't wait for a central team to hand you a golden config.

🔗 [Addy Osmani, "Agent Harness Engineering"](https://addyosmani.com/blog/agent-harness-engineering/)  
🔗 [DevOps Topologies, Anti-Type B (DevOps Team Silo)](https://web.devopstopologies.com/)

---

**Who owns your agent setup (AGENTS.md, hooks, skills)?**

🟢 My team — we tune it from our own failures  
🟡 We're using stuff from others  
🔴 Nobody really — it's ad hoc or individual  
⚪ What's a harness?

Have you as a team taken harness-building into your own hands? Any wins? Any lessons?