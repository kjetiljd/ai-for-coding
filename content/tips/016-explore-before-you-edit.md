---
title: "Tip #16: Explore before you edit"
date: 2026-03-13
categories: ["Workflow Patterns"]
weight: 16
summary: ""
---

Jumping into unfamiliar code? Before you change anything, use the agent as a research assistant.

Ask it to build you a mental map: "What are the main modules? How does data flow from API to database? Where is auth handled? What testing patterns does this project use?" You'll get a guided tour that would take an hour of reading to piece together yourself.

The agent is better at exploring when you tell it not to change anything. It won't be tempted to "fix" things along the way, and you'll have a clearer picture before you start.

In Copilot CLI, the explore subagent is purpose-built for this — it runs in a separate context window so your main session stays clean. (In Copilot Chat, @workspace gives codebase awareness in VS Code.)

💡Try this: Next time you are going to do changes in unfamiliar code, spend 5 minutes asking the agent questions about the codebase before you make any changes.
🔗 How Copilot understands your codebase (VS Code docs)


---

How do you approach unfamiliar code?
🟢 I ask the AI to explain it first  
🟡 I read the code myself, then ask AI for specifics  
🔴 I jump in and figure it out as I go  
⚪ I mostly work in code I already know

What's a good first question to ask about an unfamiliar codebase? 🧵