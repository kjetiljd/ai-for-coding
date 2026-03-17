---
title: "Tip #8: Teach your AI agent repeatable skills"
date: 2026-03-06
categories: ["Instruction Files"]
weight: 8
summary: ""
---

Instruction files (Tips [Tip #1](/ai-for-coding/tips/001/), [Tip #2](/ai-for-coding/tips/002/), [Tip #5](/ai-for-coding/tips/005/)) tell the AI how to behave in general. _But what about specific tasks you do repeatedly — deploying, writing release notes, running a particular code review checklist?_

That's what **Agent Skills** are for. A skill is a folder with a `SKILL.md` file containing step-by-step instructions for a specific task. The agent loads it only when relevant — keeping your context lean.

Skills are an open standard ([agentskills.io](http://agentskills.io)) created by Anthropic and now supported by Copilot CLI, Claude Code, and OpenCode. You write a skill once and it works across agents.

The format is simple: YAML frontmatter with `name` and `description`, then markdown instructions. The agent reads descriptions at startup and decides when to load the full instructions. You can also invoke a skill directly with `/skill-name`.

Think of instruction files as _who you are_, and skills as _what you know how to do_.

💡 Try this: Identify a task you do repeatedly (e.g. "create a PR with our template"). Write a `SKILL.md` for it in `.claude/skills/your-task/`.

(`.claude/skills/your-task/SKILL.md` is supported by Copilot CLI, OpenCode and Claude Code, see next tip!)

🔗 Spec: [https://agentskills.io/specification](https://agentskills.io/specification)  
 🔗 Copilot CLI skills: [https://docs.github.com/en/copilot/how-tos/copilot-cli/customize-copilot/create-skills](https://docs.github.com/en/copilot/how-tos/copilot-cli/customize-copilot/create-skills)


---

🟢 Yes — we have skills in our team  
🟡 I have tried it  
🔴 Nope, not yet  
⚪ Nope, I have heard agents don't use them ...

_Have you tried writing a skill? Or found a good one to share?_ _🧵_