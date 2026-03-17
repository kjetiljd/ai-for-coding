---
title: "Tip #14: Your CLI tools are already AI tools"
date: 2026-03-11
categories: ["Tools & Integrations"]
weight: 14
summary: ""
---

Here's a pattern worth noticing: your agent can use `gh`, `git`, `jq`, `curl`, `rg`, and `make` — tools already on your machine — without any MCP server, config, or setup.

Simon Willison put it well: "Almost everything I might achieve with an MCP can be handled by a CLI tool instead. LLMs know how to call `cli-tool --help`, which means you don't have to spend many tokens describing how to use them — the model can figure it out later when it needs to."

This matters because of how agents discover tool capabilities. MCP loads all tool descriptions upfront — every turn, every token. CLI tools are lazy-loaded: the agent calls `--help` only when it actually needs the tool. That's a significant context window difference when you're working on a large codebase.

Claude Code leaned into this hard — they deleted their built-in `LS` tool and replaced it with shell `ls`. OpenAI Codex shipped with no built-in file tools at all, using `sed`, `cat`, and `ls` for everything.

The practical advice: before building or installing an MCP server, check if a CLI tool already does what you need. Often, it does.

💡 Try this: Ask your agent "list my open PRs" — it will use the `gh` CLI (you might need to give a hint). No MCP needed.
🔗 Simon Willison on CLI vs MCP: [https://simonwillison.net/2025/Oct/16/claude-skills/](https://simonwillison.net/2025/Oct/16/claude-skills/)

_How does your agent interact with external tools?_  

---

🟢 Mostly CLI tools — gh, git, jq, etc.  
🟡 Mix of CLI and MCP  
🔴 Mostly MCP servers  
⚪ Haven't thought about it

_Which CLI tools have been most valuable so far?_