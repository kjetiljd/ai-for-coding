---
title: "Tip #21: Meet OpenCode — the open source coding agent"
date: 2026-03-18
categories: ["Tools & Integrations"]
weight: 21
summary: ""
---

*Most coding agents lock you into one provider. Claude Code needs an Anthropic subscription. Copilot CLI needs GitHub. What if you want to switch models — or use several?*

OpenCode (opencode.ai) is an open source coding agent that works with 75+ providers. The interesting part for us: it can use your existing GitHub Copilot license. Set your GITHUB_TOKEN, pick a model (Claude Sonnet, GPT-4o, Gemini — whatever Copilot gives you access to), and you're running.

It has a fast terminal UI, a desktop app, built-in LSP for 35+ languages (your agent actually understands your types and imports), and a Plan/Build mode split that feels natural — plan read-only first, then let it build.
120k+ stars on GitHub. Growing fast. Worth knowing about even if you don't switch — the landscape is moving toward provider-agnostic tools, and having options keeps you flexible.

💡 Try this: brew install anomalyco/tap/opencode — then run opencode in a project folder. It'll auto-detect your language server and project context.
🔗  opencode.ai — OpenCode: the open source AI coding agent

---

**Have you tried any coding agent besides Copilot?**

🟢  Yes — I use alternatives regularly (but mostly outside work)  
🟡  Tried one or two, still mostly on Copilot (at work)  
🔴  Copilot only — haven't explored others  
⚪  Not using any coding agent yet

*Which alternatives have you looked at? What pulled you in?*