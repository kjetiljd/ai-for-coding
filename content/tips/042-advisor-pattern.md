---
title: "Tip #42: The advisor pattern — frontier quality at fraction of cost"
date: 2026-06-15
categories: ["Workflow Patterns"]
weight: 42
summary: "A small, fast model executes; a powerful model sits as a callable advisor. Eve Legal: £110 → £11 per run (10×). The structure of your harness matters more than the strength of your model."
---

_Bigger model_ ≠  _better results_. The structure of your harness can matter more than the strength of your model.

Here's a model selection pattern from Anthropic's developer conference that makes this concrete. A small, fast model — Sonnet or Haiku — does all the execution. A larger, more capable model sits in the tools array, available to be called when the executor gets stuck. This is _the advisor pattern_: the powerful model is consulted, not driving.

A live demo at Code with Claude London showed what this unlocks. Eve Legal had a legal document analysis pipeline running on Opus alone: roughly £110 per run. They restructured: Sonnet executes, Opus sits in the tools array, called only on hard cases. New cost: £11. Ten times cheaper — and Opus still caught everything it would have caught before.

Another finding from the same conference: a three-prompt loop on Sonnet (generate → evaluate → repair) beat Opus with adaptive thinking on tokens, latency, and pass rate. Cheaper, faster, better.

The practical takeaway: before reaching for a bigger model, ask if a smarter workflow with a smaller model gets you there. And as billing becomes more usage-based (see tip #41 on tracking AI costs), the economics of this are only getting sharper.

Note: This pays off most on repeatable tasks — document review, code generation loops, CI checks — where you can measure cost per run and tune model choice against outcome quality. One run on Opus can tell you if Sonnet can handle it. If it can, every subsequent run is cheaper.

💡 Try this: If you have a complex agent task that you run repeatedly and it feels expensive, try adding a "review" step using a stronger model as a tool call — rather than running the whole pipeline on the strong model. Measure the difference over a few runs before committing to either approach.

🔗 [Code with Claude London — advisor pattern demo](https://youtu.be/QIriO1-vHYw?t=1168)  
🔗 [Eve Legal case study](https://youtu.be/6amLO7I9xdg?t=1350)

---

**How do you choose models for agent tasks?**

🟢 Match the model to the task complexity  
🟡 Haven't thought about it, I use whatever the tool defaults to  
🔴 Always use the best model available  
⚪ I rarely do things the same way twice

_Tried the advisor pattern? Share what you found 🧵_