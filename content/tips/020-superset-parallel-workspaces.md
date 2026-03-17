---
title: "Tip #20: Give your agents their own workspaces"
date: 2026-03-17
categories: ["Workflow Patterns"]
weight: 20
summary: ""
---

_[Tip #19](/ai-for-coding/tips/019/)_ _covered using fresh agent sessions for second opinions. But what if you want multiple agents working at the same time — on different tasks, in the same repo? That's an orchestration problem._

You need isolated environments so agents don't overwrite each other's changes, a way to see what each one is doing, and an easy path to review and merge the results.

**Superset** (superset.sh) is a macOS app built for exactly this. It spins up isolated workspaces for each agent (using git worktrees under the hood), gives each its own terminal, shows you diffs, and lets you open any workspace in VS Code or JetBrains.

It's agent-agnostic — Copilot CLI, Claude Code, whatever CLI agent you have.

The workflow: give three agents three different tasks, let them run in parallel, review each result separately, merge what's good. What used to be a manual juggling act becomes a dashboard.

💡 Try this: Check out superset.sh if you're running multiple agents. Or try the pattern manually: `git worktree add ../my-feature feature-branch` gives an agent its own isolated copy of the repo.
🔗 [superset.sh](https://superset.sh/) — Superset: parallel agent workspaces

_Where does your coding agent live?_  

---

🟢 Multiplexing terminal (tmux, Superset, Warp, etc.)  
🟡 In a terminal (standalone or IDE integrated)  
🔴 Chat pane in my IDE (Copilot Chat, Cursor, etc.)  
⚪ Web only (ChatGPT, [Claude.ai](http://Claude.ai), etc.)

_What's your setup — one agent at a time, or multiple in parallel?_