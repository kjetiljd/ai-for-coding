---
title: "Tip #35: Spike first, build second"
date: 2026-05-19
categories: ["Limits & Failure Modes"]
weight: 35
summary: "AI makes implementation cheap — use that to run more experiments. Treat the first pass as a throwaway spike, then start fresh and build with intention."
---

_The agent built the feature in 20 minutes. It compiles, tests pass. Two weeks later you're refactoring the whole thing because the design was wrong from the start._

When AI handles the typing, you can move faster — and faster means you can afford more experiments. More experiments means more learning. Experienced developers are leaning into this: **treat the first pass as a spike** — throwaway code whose only purpose is to answer a question about the problem.

Let the agent explore the solution space fast. Don't agonise over structure. The goal isn't production code, it's discovery: Where do the design decisions cluster? What are the real trade-offs? What did you _actually_ need?

Why? AI picks whatever is locally plausible. It doesn't know you're optimising for maintainability over speed, or that three teams will share this module. One engineer's post-mortem after months of AI-heavy work: _"I spent weeks following AI down dead ends. In hindsight, it might have been faster just thinking it through."_

Then start fresh. Anthropic's own best-practices documentation says it plainly: _"A clean session with a better prompt almost always outperforms a long session with accumulated corrections."_ The spike gave you the understanding; the second pass gets your architecture.

💡 Next time you start something non-trivial: timebox a spike, extract what you learned, then `git stash` and build for real in a fresh session.
🔗 [Lalit Maganti — "Eight years of wanting, three months of building with AI"](https://lalitm.com/post/building-syntaqlite-ai/)

---

**Do you ever intentionally throw away AI-generated code?**

🟢 Yes — spike then rebuild is my normal flow  
🟡 Sometimes, when I realise the structure was wrong  
🔴 No — I refactor what the AI gives me  
⚪ Hadn't considered this approach

_What's the biggest thing you've thrown away and rebuilt?_