---
title: "Tip #9: Where to put your skills (and where they'll actually be found)"
date: 2026-03-06
categories: ["Instruction Files"]
weight: 9
summary: ""
---

You've written a SKILL.md ([Tip #8](/ai-for-coding/tips/008-agent-skills-intro/)). Now where do you put it?

Skills have two scopes: project (committed to the repo, shared with the team) and personal (in your home directory, often available across all projects).

For project skills:

- Copilot CLI looks in `.github/skills/` or `.claude/skills/`.
- Claude Code uses `.claude/skills/`.
- OpenCode checks `.opencode/skills/`, `.claude/skills/`, and `.agents/skills/`.



The practical takeaway: `.claude/skills/` works across all three agents today. If you want maximum portability, use that path. For personal skills, `~/.claude/skills/` is similarly cross-agent.

One thing to know: the Agent Skills spec ([agentskills.io](http://agentskills.io)) defines the file format — not where to put them. The `.claude/` convergence happened because Claude Code was first to market and others chose compatibility. OpenCode's `.agents/skills/` is the first attempt at a vendor-neutral path. This may evolve.

Org/enterprise-level skills? GitHub says "coming soon." Claude Code supports it via managed settings.

💡 Try this: Run `/skills list` in Copilot CLI to see what skills are already discovered in your project.

🔗 [Copilot CLI skill paths](https://docs.github.com/en/copilot/concepts/agents/about-agent-skills)  
🔗 [Open standard](https://agentskills.io/specification)


---

🟢 I use both personal and project skills  
🟡 I use personal or project skills  
🔴 I use neither, yet  
⚪ I find that skills still don't really work ...

_What is your best personal skill doing?_