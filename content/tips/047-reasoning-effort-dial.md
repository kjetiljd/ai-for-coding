---
title: "Tip #47: Turn the thinking dial (reasoning effort)"
date: 2026-07-10
categories: ["Model Selection"]
weight: 47
summary: "Model choice is one lever; how hard the model thinks is another. Reasoning effort (low→xhigh) can matter more than model size — a mid-tier model thinking hard often beats a big one thinking little. In Copilot, set it in the /model picker with ←/→."
---

Picking a model is one lever ([Tip #46](/ai-for-coding/tips/046-match-model-to-task/)). There's a second one: how hard the model thinks. Most modern models expose a reasoning-effort setting — low → medium → high → xhigh/max — trading latency and cost for depth. (Some even have a none setting for extra speed.)

Rough guide, straight from OpenAI's and Anthropic's docs:
- low — execution-oriented coding, simple edits, drafting
- medium — everyday agentic coding (a solid default)
- high / xhigh — hard debugging, deep planning, security and code review

The counterintuitive part: reasoning effort can matter more than model size. A mid-tier model thinking hard can beat a bigger model thinking little. Anthropic says it plainly: "Tuning effort is often a better lever than switching models."

Caveat: thinking isn't free — and at high effort, models might over-engineer, adding refactors and abstractions you didn't ask for. It also takes longer.

Where's the dial? In Copilot, open /model and use ←/→ to set the reasoning effort for the highlighted model. Claude Code has /effort.

💡 Try this: A/B test it on one model. Set the lowest reasoning effort, give it a task, notice the outcome. /rewind to reset, then set the same model to the highest reasoning level and give it the same task. Do the results differ? Did it take longer?

🔗 [Anthropic effort guide](https://platform.claude.com/docs/en/build-with-claude/effort)  
🔗 [OpenAI reasoning](https://developers.openai.com/api/docs/guides/reasoning)

---

**Have you tuned reasoning effort?**

🟢 Yes, it's part of my workflow  
🟡 Tried it once or twice  
🔴 Haven't thought much about it (my reasoning effort was low 😁)  
⚪ I am going to try it now!

What did you observe from the 💡 Try this-experiment?