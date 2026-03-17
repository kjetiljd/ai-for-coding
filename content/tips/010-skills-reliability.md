---
title: "Tip #10: Why your skills might not be triggering"
date: 2026-03-06
categories: ["Instruction Files"]
weight: 10
summary: ""
---

You wrote a skill (Tip #8), placed it right (Tip #9), but the agent doesn't use it. You're not alone.

Vercel's engineering team ran rigorous evals on this. With default settings, the agent **never invoked the skill in 56% of cases** — even though it was available. Adding explicit instructions ("explore the project first, then invoke the skill") raised usage to 95% and pass rate from 53% to 79%. But an 8KB docs index embedded directly in `AGENTS.md` hit **100%** — no skill invocation needed.

Their theory: passive context (AGENTS.md) has no decision point — the info is just *there*. Skills require the agent to decide "should I look this up?" and current models aren't reliable at that step.

The practical takeaway: use skills for **tasks you invoke explicitly** — deploy, release, code review checklists. For general knowledge the agent should always have (coding patterns, API docs, framework conventions), put it in `AGENTS.md` instead. Horizontal knowledge → instruction file. Vertical procedures → skills.

💡 Try this: In Copilot CLI, run `/skills list` and check descriptions. Are they specific enough for the agent to know when to trigger? Vague descriptions = missed activations.

🔗 Vercel's full analysis: https://vercel.com/blog/agents-md-outperforms-skills-in-our-agent-evals

Experienced skills not triggering? Found a workaround?