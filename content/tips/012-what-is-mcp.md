---
title: "Tip #12: MCP — the USB-C of AI tools"
date: 2026-03-10
categories: ["Tools & Integrations"]
weight: 12
summary: ""
---

Model Context Protocol (MCP) is an open standard for connecting AI agents to external systems. Think of it as USB-C for AI: one standard plug, many devices.

Without MCP, agent-tool integrations are custom. With it, an MCP server written once works across Copilot CLI, Claude Code, Cursor, VS Code, JetBrains — any MCP-compatible client. The protocol handles tool discovery, invocation, and data exchange.

In Copilot CLI, you already have one MCP server: the GitHub MCP server (pre-configured). Adding more is straightforward — type `/mcp add`, give it a name, and point it at a command like `npx some-mcp-server@latest`. The server starts as a local process and exposes tools the agent can call.

The ecosystem is growing fast. GitHub now has an MCP Registry — a curated directory of servers you can browse. Database tools, cloud providers, monitoring systems, calendars — if it has an API, someone's probably built an MCP server for it.

A heads-up: MCPs aren't free. Each server adds tool descriptions to your context window — every turn, from the first prompt. Too many servers and your agent spends its working memory on tool menus instead of your code. And sometimes a plain CLI tool already on your machine does the same job with zero setup. More on that in a future tip.

💡 Try this: In Copilot CLI, type `/mcp` to see your connected servers and their tools. Then browse the registry at [github.com/modelcontextprotocol](https://github.com/modelcontextprotocol)

🔗 [MCP intro](https://modelcontextprotocol.io/introduction)

_How's your MCP journey?_  

---

🟢 Already using MCP servers beyond the built-in one  
🟡 Aware of MCP but haven't added any yet  
🔴 Tried it, ran into issues  
⚪ First time hearing about this

_Using any MCP servers beyond the GitHub one? Which ones?_