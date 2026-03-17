---
title: "Tip #13: Give your agent a browser"
date: 2026-03-10
categories: ["Tools & Integrations"]
weight: 13
summary: ""
---

One of the most practical MCP servers gives your agent what it's been missing: a browser.

Chrome DevTools MCP (chrome-devtools-mcp) lets your agent open pages, click buttons, fill forms, read console logs, inspect network requests, take screenshots, and even run Lighthouse performance audits — all from your terminal.

It's built by the Chrome DevTools team at Google — 27,000+ stars on GitHub — and works with Copilot CLI, Claude Code, Cursor, IntelliJ, etc.

Real use cases: debugging a frontend issue by having the agent inspect console errors and network requests. Running performance traces on your staging environment. Filling out and testing forms across different viewports. Navigating internal tools that don't have APIs.

Setup in Copilot CLI takes 30 seconds: type /mcp add, name it chrome-devtools, set the command to npx -y chrome-devtools-mcp@latest. Done. The server starts a Chrome instance when the agent first needs it.

Microsoft's Playwright MCP is the other major option (28,000+ stars). However, the Playwright team now recommends their CLI+Skills approach over MCP for coding agents — calling it "more token-efficient." The trade-off between MCP and plain CLI tools deserves its own tip — stay tuned.

💡 Try this: After setup, ask your agent: "Open https://your-staging-site.com and check if there are any console errors."
🔗 [Chrome DevTools MCP](https://github.com/ChromeDevTools/chrome-devtools-mcp)  
🔗 [Playwright CLI](https://github.com/microsoft/playwright-cli)


---

**Have you given your coding agent proper browser access?**

🟢 Yes — it's a game changer  
🟡 Interested, haven't tried yet  
🔴 Sounds risky, not sure I want that  
⚪ Didn't know this was possible

What did/would you point an agent-with-a-browser at first?