---
title: "Tip #23: Write scripts that guide the agent"
date: 2026-03-19
categories: ["Workflow Patterns"]
weight: 23
summary: "Script output goes straight into the agent's context window. Design it to say what happened and what to do next — not just what ran."
---

_[Last tip](/tips/022-deterministic-scripts/) covered using scripts for repeatable tasks. But what the script prints back matters a lot._

When an agent runs a script, the output goes straight into its context window. A wall of logs wastes tokens and confuses next steps. A few clear lines — _"3 tests failed: X, Y, Z"_ or _"Deploy complete. DB migrated to v12."_ — tells the agent exactly what to act on.

Design your scripts like you're writing with compassion for a fellow dev: **what happened, what to do next.** Suppress verbose output by default. Summarize results. Flag what needs attention.

You can go further: pair scripts with instructions. Add a note in your instruction file: _"After running reset-dev.sh, check the output for migration errors before continuing."_ Now the script and the instructions tell the agent how to react. Another option for filtering output is using a "postToolUse" hook. More on that later.

💡 Try this: Look at a script the agent uses. Is the output helpful, or is it noise? Add a summary line at the end that says what happened and what to do next.

---

**How much do you think about script output when working with an agent?**

🟢 Actively — I design output for the agent  
🟡 A little — I've trimmed some noisy output  
🔴 Not at all — hadn't considered it  
⚪ I don't use scripts with agents yet

_Got a good example of agent-friendly script output?_