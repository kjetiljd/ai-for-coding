---
title: "Tip #6: Your terminal just got an AI agent"
date: 2026-02-26
categories: ["Getting Started with GitHub Copilot"]
weight: 6
summary: "Copilot CLI brings agentic coding to your terminal — reads files, runs commands, makes changes."
description: "Copilot CLI brings agentic coding to your terminal — reads files, runs commands, makes changes."
---

A year ago, Boris Cherny at Anthropic released **Claude Code** internally — a terminal-based AI agent that doesn't just suggest code, but reads files, runs commands, and makes changes across your project. Boris claims the terminal UI (Text UI - TUI) agent pattern is here to stay.

GitHub **Copilot CLI** brings the same idea to our toolchain. Install it:

brew install copilot-cli

Then type `copilot` in any project directory to start a session.

It can read your code, edit files, run shell commands, and interact with GitHub — create PRs, work on issues, the lot. It reads your `copilot-instructions.md` and `AGENTS.md` ([Tip #1](/ai-for-coding/tips/001-copilot-instructions/)) and supports plan mode ([Tip #3](/ai-for-coding/tips/003-sparring-partner-plan-mode/)). When it wants to run something, it asks permission first.

The shift from "AI suggests a line" to "AI works on a task" is the big one. Terminal agents are where that shift is happening fastest.

💡 Try this: Install Copilot CLI and start a session in a project. Ask it to explain the codebase before asking it to change anything.

🔗 [Install](https://docs.github.com/en/copilot/github-copilot-in-the-cli/installing-github-copilot-in-the-cli)  
🔗 [Docs](https://docs.github.com/en/copilot/concepts/agents/about-copilot-cli)

---

**Have you tried a terminal-based AI agent?**

🟢 Yes — I use one regularly  
🟡 Tried it, still figuring it out  
🔴 Not yet, but curious  
⚪ I prefer staying in the IDE

_What's been your experience?_