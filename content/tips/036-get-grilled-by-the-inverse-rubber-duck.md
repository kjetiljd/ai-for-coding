---
title: "Tip #36: Get grilled by the inverse rubber duck"
date: 2026-05-20
categories: ["Planning & Design"]
weight: 36
summary: "Before coding, have the agent interview you about the plan. The inverse rubber duck asks the hard questions — surfacing gaps and assumptions when they're cheap to fix."
---

_Rubber duck debugging works because explaining forces clarity. But what if the duck talked back — and asked the hard questions?_

Before writing code, have the agent grill _you_ about the plan. A [recent study](https://arxiv.org/abs/2603.26233) indicate that coding agents which ask clarifying questions first score higher on ambiguous tasks. The pattern is simple: tell the agent to interview you relentlessly, one question at a time.

Here's a prompt you can use directly (from Matt Pocock's open-source `/grill-me` skill):

> Interview me relentlessly about every aspect of this plan until we reach a shared understanding. Walk down each branch of the design tree, resolving dependencies between decisions one-by-one. For each question, provide your recommended answer.
>
> Ask the questions one at a time.
>
> If a question can be answered by exploring the codebase, explore the codebase instead.

Gaps, contradictions, and unstated assumptions surface before any code is written — when they're cheap to fix.

💡 Try this next time you have a non-trivial task: paste the prompt above before writing any code. Answer until the agent has nothing left to ask — then build.
🔗 [Matt Pocock's /grill-me skill](https://github.com/mattpocock/skills/blob/main/skills/productivity/grill-me/SKILL.md)

---

**When do you most often wish you'd thought harder before coding?**

🟢 Designing APIs or data models  
🟡 Multi-file refactors  
🔴 Integrations with external systems  
⚪ I just start and fix as I go

_Have you tried something like this? How did it go?_