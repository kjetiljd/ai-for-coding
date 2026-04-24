---
title: "Tip #31: Review your code through different lenses"
date: 2026-04-24
categories: ["Code Review"]
weight: 31
summary: "Run separate review passes with different expert frames — security, architecture, framework. Each 'lens' activates different model knowledge."
---

A colleague shared a pattern: after implementation, she runs separate review passes with different expert reviewers.

- *"Review this as a security expert — focus on injection, auth, secrets"*
- *"Review this as a [your framework] developer — what's non-idiomatic?"*
- *"Review this as a system architect — where's the coupling?"*

Security and QA/testing consistently catch the most issues that normal review misses — hardcoded secrets, race conditions, untested edge cases. Each expert framing activates different model knowledge.

Totto ([wiki.totto.org](https://wiki.totto.org/blog/2026/04/15/two-architectures-for-claude-code-what-19700-stars-got-right-and-what-they-missed/#the-skills-revelation)) calls this a *lens* — a prompt that doesn't tell the agent what to *do*, but how to *think*. Most agent skills are actions: "run tests", "format code." A lens is different. A Kent Beck lens doesn't say "write tests first." It says *"think about design as the activity that testing enables."* It shifts the reasoning frame, not the action list. What she does intuitively — switching between a security expert and an architect — is exactly this: swapping lenses.

If you use subagents ([Tip #27](/ai-for-coding/tips/027-subagents/)), each reviewer gets its own fresh context — no cross-contamination between lenses.

💡 **Try this:** After your next PR, ask the agent: *"Review this diff as a security expert. Focus on OWASP Top 10, injection, auth, and hardcoded secrets."* Then start a fresh session and ask for an architecture review.

🔗 [Totto on action skills vs lens skills](https://wiki.totto.org/blog/2026/04/15/two-architectures-for-claude-code-what-19700-stars-got-right-and-what-they-missed/#the-skills-revelation)

---

**How do you review AI-generated code today?**

🟢 I review it carefully myself + I use AI to review  
🟡 I review it carefully myself  
🔴 I rely on AI to do it (Copilot PR review, ...)  
⚪ I hadn't thought about using the AI to review its own output

Tried a "lens" that works well? 🧵