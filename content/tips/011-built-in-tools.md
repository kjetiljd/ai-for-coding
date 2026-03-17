---
title: "Tip #11: What your agent already knows how to do"
date: 2026-03-09
categories: ["Tools & Integrations"]
weight: 11
summary: ""
---

Before you install anything extra, your coding agent already comes with tools. Copilot CLI ([Tip #6](/ai-for-coding/tips/006/)) ships with built-in tools for reading files, editing code, searching your codebase (grep, glob), and running shell commands. It can also delegate to subagents — spinning up separate context windows for exploration, code review, or long-running tasks like test suites.

And it ships with the GitHub MCP server pre-configured. That means `list my open PRs`, `check the CI status`, or `create an issue` work from day one — no setup.

You can see what's available: ask the agent `**list all your tools**` and it will usually list its capabilities.

Use `/mcp` to see connected MCP servers and their tools, and `/context` to see how much of your context window tools are consuming. The `!` prefix runs shell commands directly, bypassing the model entirely — handy for quick `git status` or `ls` checks.

The point: many start looking for plugins and extensions before exploring what's already there. The built-in tools cover a surprising amount of daily work — file operations, code search, shell access, GitHub integration.

💡 Try this: Open Copilot CLI and ask: `**List all your tools and what each one does.**` You might be surprised what's already loaded.

🔗 Full feature reference: [https://docs.github.com/en/copilot/concepts/agents/copilot-cli/comparing-cli-features](https://docs.github.com/en/copilot/concepts/agents/copilot-cli/comparing-cli-features)

_How much of the built-in toolset have you seen being used?_

---

🟢 The works — edits, web stuff, shell, subagents, planning, GitHub MCP ...  
🟡 Some — mostly file edits and shell commands  
🔴 Barely scratched the surface  
⚪ I don't use Copilot CLI, but my agent uses similar tools (anything cool? share in 🧵 !)

_What built-in tool surprised you the most? Positively or negatively?__🧵_