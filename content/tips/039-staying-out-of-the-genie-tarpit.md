---
title: "Tip #39: Staying out of the genie tarpit"
date: 2026-05-27
categories: ["Limits & Failure Modes"]
weight: 39
summary: "Kent Beck: AI agents push code down and to the left — less working, less changeable. The agent delivers features; flexibility is still yours to maintain."
---

Kent Beck frames software value on two axes: **features** (does it work?) and **flexibility** (can we change it safely?). His claim is that many teams were not really having the capacity to do proper __engineering__ before AI - they were __muddling__ — things were mostly working, but somewhat hard to change. His observation: AI agents push you further down and left.

![Kent Beck's Features vs Flexibility grid — genies live down and to the left](/images/genie-tarpit-beck.jpg)
*Source: Kent Beck, [Genie Tarpit](https://tidyfirst.substack.com/p/genie-tarpit)*

> The 'plausible deniability' task orientation of the genie leaves it claiming success even though the code doesn't work at all. And complexity piles on complexity until even the genie can't pretend to make progress any more.

GitClear's data backs this up: refactoring dropped from 25% to under 10% of code changes since 2021, while copy-pasted code doubled. Teams are investing less in changeability — and the AI makes it easy not to notice, because the flexibility axis has a wide operating range. You can skimp for a while before feeling it.

The escape route runs through this series: e.g verify the agent's work ([tip #33](/tips/033-agent-verification/)), read for comprehension not just correctness ([tip #29](/tips/029-comprehension-debt/)), review through different lenses ([tip #31](/tips/031-review-lenses/)), and own the architecture ([tip #25](/tips/025-engineering-skills-shifted/)). The agent delivers features. Flexibility is still yours to maintain.

🔗 [Kent Beck — Genie Tarpit](https://tidyfirst.substack.com/p/genie-tarpit)  
🔗 [GitClear AI Code Quality report](https://www.gitclear.com/ai_assistant_code_quality_2025_research)

---

**Where is your code on Beck's grid?**

🟢 Upper-right — we invest in both features and flexibility  
🟡 Muddling — things mostly work, but change is hard  
🔴 Sliding left — AI is fast, but the code is getting harder to change  
⚪ Haven't thought about it this way

_How do you maintain code flexibility with AI?