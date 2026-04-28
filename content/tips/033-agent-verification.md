---
title: "Tip #33: Give your agent a way to check its own work"
date: 2026-04-28
categories: ["Workflow Patterns"]
weight: 33
summary: "Tell the agent to run tests, type checkers, and linters after changes. Without verification tools, you're the only feedback loop."
---

_An agent without verification tools is ... guessing ... and you become the only feedback loop. Every mistake requires your attention._

The fix is simple: tell the agent how to verify. Add this to your instruction file (CLAUDE.md, copilot-instructions.md, .cursorrules, AGENTS.md — whatever your tool uses):

```
After making code changes:
- Run tests (`add command here`) and fix any failures
- Run the linter (`linter command here`)
- Do NOT modify existing test assertions to make them pass
```

That last line might help catch cases where the agent may "fix" failing tests by changing the assertions instead of fixing the code. The tests pass, CI is green, and the bug ships.

Research backs this up: giving an LLM execution feedback (test results, error messages) improves code accuracy by up to 12% (Chen et al., "[Self-Debugging](https://arxiv.org/abs/2304.05128)"). The agent sees *what* failed and *why* — and self-corrects.

The verification is only as good as your test suite. If coverage is 20%, passing tests tells you almost nothing about the other 80%. The strongest setup: you write the tests, the agent makes them pass.

Later on you can consider creating subagents/skills/hooks to further increase the effectiveness and adherence to the verification process.

💡 **Try this:** Add the three lines above to your instruction file. Next time the agent makes a change, watch whether it runs the tests itself.

---

**How does your agent verify its work today?**

🟢 I include verification steps in my instruction file  
🟡 I ask it to run tests when I remember  
🔴 I verify everything manually myself  
⚪ I hadn't thought about this

What verification setup do you give your coding agent? 🧵