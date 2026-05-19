---
title: "Tip #34: Ask for HTML, not just text"
date: 2026-05-19
categories: ["Workflow Patterns"]
weight: 34
summary: "Before a big change, ask the agent for the plan as HTML and open it in your browser."
---

When a coding agent proposes a big change — a refactor, a file restructure, a dependency upgrade — you're reviewing the plan inside a chat window. A recent study (arxiv:2505.10742) found that the chat interface itself becomes the obstacle: walls of text, easy to miss details, iteration gets messy.

The fix is surprisingly simple: ask for the plan as HTML and open it in your browser.

```
Before you make any changes, create an HTML review report for this task: [TASK].
Include:
- Proposed actions (table: action, target path, reason)
- Before/After structure (tree view)
- Risks & edge cases
- Open questions
Output only valid HTML. Do not execute anything yet.
```

Why HTML? Anthropic's Claude Code team internally switched to HTML as the default output for plans and reviews. As one engineering lead put it: you get headings, tables, collapsible sections, even inline SVG diagrams — things that make you spot architectural issues in 30 seconds that take 30 minutes in a markdown wall.

You're not replacing markdown for everything — just for the review step before irreversible execution. The HTML is ephemeral: review it, iterate, approve, move on.

💡 **Try this:** Next time you ask an agent for a multi-file change, add "Output the plan as HTML first. Do not execute yet." Open it in your browser. Iterate until you're confident, then approve.

🔗 [Examples](https://thariqs.github.io/html-effectiveness/)

---

**Where do you most need a "review report" before letting the agent loose?**

🟢 Code changes (multi-file refactors)  
🟡 Repo hygiene (moves, renames, deps)  
⚪ Cloud/infra changes  
🔴 Data/files (migrations, cleanups)

Tried HTML output? Share your experience 🧵