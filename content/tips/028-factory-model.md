---
title: "Tip #28: Are we building a factory?"
date: 2026-04-20
categories: ["Beyond Copilot / Team & Culture"]
weight: 28
summary: "The 'factory model' for AI coding is everywhere. But our industry has tried to industrialise software five times before. Each wave made something easier. None solved it. Is this time different?"
---

"You are no longer just writing code. You are building the factory that builds your software."
— Addy Osmani, paraphrasing Cursor CEO Michael Truell

This idea is everywhere right now. Agents run in parallel, PRs are auto-generated, humans orchestrate instead of typing. It sounds compelling. But our industry has heard this pitch before.

In the 1970s, the Waterfall model promised factory-style predictability and was based on a paper whose author actually warned against it. In the 1980s, CMM tried to make software quality "measurable like manufacturing" and produced organisations that passed audits without changing how they actually worked. Japan built literal software factories at Hitachi and NEC: they worked for stable, well-understood domains but couldn't produce innovation. CASE tools, 4GLs, UML code generation, low-code ... each wave promised to industrialise software. Each made something easier. None solved it.

Call it the Production Fallacy: the recurring belief that the bottleneck in software is producing code, not deciding what to produce. Fred Brooks nailed it in 1986: the hard part is essential complexity (understanding the problem). Jack Reeves put it sharply in 1992: source code IS the design, compiling is just duplication, and it's nearly free. There is no separate "manufacturing" phase to optimise.

So what's different this time? Honestly, something is different. AI works on natural language and messy real codebases, not formal models. It doesn't try to standardise human work, it replaces routine production and keeps humans for judgment.

But the early data is sobering. Greptile's State of AI Coding report shows lines of code per developer tripled, while CodeRabbit found AI-generated PRs contain 1.7× more bugs and 75% more logic errors than human-authored code. Global outages rose 32% in Q1 2025. The factory is producing more. Whether "more" is what we need is the question.

:thinking_face: Food for thought: Are we designing a functioning factory? Or are we repeating a 50-year-old mistake with better tools?

🔗 [Osmani — "The Factory Model"](https://addyosmani.com/blog/factory-model/)  
🔗 [Brooks — "No Silver Bullet" (1986)](https://en.wikipedia.org/wiki/No_Silver_Bullet)  
🔗 [CodeRabbit — AI vs Human Code Generation](https://www.coderabbit.ai/blog/state-of-ai-vs-human-code-generation-report)

---

**Where do you land?**

🟢 The factory metaphor fits — we need to embrace it and invest in quality gates  
🟡 Something has changed, but "factory" is the wrong word for it  
🔴 We've seen this movie before — it won't end differently  
⚪ I don't think about metaphors, I just ship code

What does your experience tell you?