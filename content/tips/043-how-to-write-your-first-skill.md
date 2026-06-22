---
title: "Tip #43: How to write your first skill"
date: 2026-06-19
categories: ["Workflow Patterns"]
weight: 43
summary: "Two paths to writing skills: translate existing runbooks or ask the agent to draft from a successful trace. The description field is the routing algorithm. Anthropic's skill-creator skill walks you through creation."
---

You know [what skills are](/ai-for-coding/tips/008-teach-your-agent-a-new-skill) and [where to put them](/ai-for-coding/tips/009-where-do-skills-live). Now: how do you actually write one?

Two paths plus a skill for creating skills:

Path A — Translate what you already have. You probably already have the content: a Confluence page, a procedure, an onboarding doc, a checklist you paste in repeatedly. Now the idea is to translate it and structure it as a SKILL.md: YAML frontmatter with name and description, then your steps as markdown. Domain experts can do this without writing code.

Path B — Crystallize what the agent just did. The agent completed a non-trivial task well. You want the next run to benefit from what just happened. Ask the agent to write a SKILL.md draft from that trace — describe the workflow, structure the steps, write the description. You review instead of authoring. Anything that's a good reusable workflow can become a skill this way.

The skill-creator skill. Anthropic ships a skill-creator skill that walks you through creation, helps you write eval cases, and tunes the description until trigger accuracy is where it should be. Install it once, and it helps you build all your other skills.

Important: The description field is the routing algorithm. The agent decides whether to load your skill based solely on this text. Be specific. Front-load trigger keywords. State explicitly what it's NOT for. A vague description might cause a skill to never fire.

Btw a skill can grow beyond a single file — you can add a scripts/ folder for deterministic helper scripts, references/ for supplementary docs that load on demand, and assets/ for templates. The SKILL.md stays lean; the detail lives alongside it.

The quality bar is the same whether a human or an agent writes the first draft. A reviewed, iterated, skill can be excellent. An un-reviewed one ... well ... take time to tune your skill.

💡 Try this: Finish a task with your agent today. Before you close the session, ask it: "Write a SKILL.md for what we just did." Review the draft — especially the description field. Install it and test it with three prompts: two that should trigger it, one that shouldn't.

🔗 [Anthropic skill-creator](https://github.com/anthropics/skills/tree/main/skills/skill-creator)  
🔗 [Anthropic skills repo](https://github.com/anthropics/skills)

---

**How have you been creating skills so far?**

🟢 I write them myself from scratch  
🟡 I ask the agent to draft them  
🔴 I haven't written any yet  
⚪ I haven't really started using skills, yet

Share your best skill — what does it do?