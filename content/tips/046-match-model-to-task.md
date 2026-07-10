---
title: "Tip #46: Match the model to the task"
date: 2026-07-10
categories: ["Model Selection"]
weight: 46
summary: "Your coding agent isn't one task — planning, grinding boilerplate, hunting bugs. Run /subagents to read the Copilot team's own task→model map: cheap+fast for grinding, a different family for critique, your strong model for review. Vendors now ship the ladder."
---

We've mostly said use the best model — and for high-value one-offs, that's probably a fine default. But your coding agent isn't one task. It's many: planning, grinding out boilerplate, hunting a nasty bug, running commands. You might not need the biggest frontier model and it might even be slower.

The best cheat sheet is already in your terminal. Run `/subagents` in Copilot CLI and read the default model each subagent ships with (they are likely the default ones, if you haven't added your own):
- explore, task → Haiku — fast + cheap for high-volume grinding (search, running commands)
- research → Sonnet — a step up where synthesis matters
- rubber-duck → a different model family — a genuinely diverse second opinion
- code-review, security-review → inherit your strong driver model

That's the Copilot team's own task→model map — and notice it's not "always the biggest." The principle generalizes: a frontier model (Opus, GPT-5.6 Sol) for deep reasoning and debugging; a fast, cheap one (Haiku, GPT-5.6 Luna) for mechanical work. As one practitioner puts it: *"Use Opus to think and Sonnet to build."*

Switch your own model in Copilot with /model. Claude Code has the same idea.

💡 Try this: Run /subagents (in Copilot CLI) and read the defaults — cheap+fast for grinding, a different family for critique, your strong model for review.

🔗 [GitHub model comparison](https://docs.github.com/en/copilot/reference/ai-models/model-comparison)  
🔗 [Claude — choosing a model](https://platform.claude.com/docs/en/about-claude/models/choosing-a-model)

---

**How do you pick a model?**

🟢 I match it to the task  
🟡 I use the default / auto  
🔴 Always the best I can get  
⚪ I don't think too much about / I didn't know I could change

What's your go-to model for your main agent? Why?