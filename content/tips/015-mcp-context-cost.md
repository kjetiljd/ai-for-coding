---
title: "Tip #15: MCP servers eat your context window"
date: 2026-03-11
categories: ["Tools & Integrations"]
weight: 15
summary: ""
---

Every MCP server you connect adds tool descriptions to the agent's context — every turn, from the first prompt. Connect five servers and you can lose 30-50% of your context window before you've even asked a question.

This isn't theoretical. LangChain research found that ~10 tools is the sweet spot for model accuracy. Beyond that, the agent gets worse at choosing the right tool — the menu is too long.

Toolmakers are noticing. Claude Code recently shipped "Tool Search" — a lazy-loading system that only loads tool definitions on-demand. Anthropic reports 85-95% reduction in initial context usage. It activates automatically. Smart, but currently Claude Code-specific.

In Copilot CLI, the pattern is: be selective. Type `/context` to see your token budget. The GitHub MCP server and Chrome DevTools MCP ([Tip #13](/ai-for-coding/tips/013-browser-mcp/)) earn their context cost. But "install every MCP server that looks cool" is a trap.

And remember: if a CLI tool can do the same job ([Tip #14](/ai-for-coding/tips/014-cli-tools-are-ai-tools/)), it costs zero context until the agent calls `--help`.

💡 Try this: Run `/context` in Copilot CLI. How much of your budget is tool descriptions vs. actual conversation?

🔗 [Claude Code Tool Search](https://docs.anthropic.com/en/docs/claude-code/changelog) (search "ToolSearch")  
🔗 [GitHub docs on MCP toolsets](https://docs.github.com/en/copilot/concepts/context/mcp#toolset-customization)


---

How many MCP servers do you have connected?  

🟢 Just the GitHub one  
🟡 2-3 carefully chosen  
🔴 Lost count — maybe too many  
⚪ None yet, still figuring it out

Tips for keeping your context lean?