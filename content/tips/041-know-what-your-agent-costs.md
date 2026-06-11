---
title: "Tip #41: Agent costs rise - should you care?"
date: 2026-06-11
categories: ["Limits & Failure Modes"]
weight: 41
summary: "AI tool pricing has changed — Copilot is now usage-based, Claude Code has premium tiers. Most users are fine, but heavy agent users should check their spend with ccusage or tokscale."
---

The pricing landscape for AI coding tools has shifted. Claude Code has a new model tier (mythos-level), twice as expensive as opus. GitHub Copilot moved to usage-based billing June 1 — your use is now more or less per token, at rates that vary by model. The era of "flat rate, use all you want" is more or less over. The result is invariably that AI Agent use costs more.

Don't let this scare you off exploring & learning. Most of you shouldn't think too hard about this, as we are still learning and exploring, and have modest use. Keep experimenting, keep using AI to support your job.

However, if you're running tons of sub-agents on large codebases, or spawning long-running agentic tasks across multiple repos — that's where token burn adds up fast. A quick chat with Claude Sonnet costs pennies. A multi-agent workflow session with Claude Fable can consume a month's worth of use in an hour.

The practical move: develop cost awareness without cost anxiety. Here's how to check your actual spend (this method works for Copilot CLI, OpenCode, Claude Code CLI etc).

Step 1: Enable OpenTelemetry logging for Copilot CLI (to make it report usage in a log file):

```bash
export COPILOT_OTEL_ENABLED=true
export COPILOT_OTEL_EXPORTER_TYPE=file
export COPILOT_OTEL_FILE_EXPORTER_PATH="$HOME/.copilot/otel/copilot-otel-$(date +%Y%m%d-%H%M%S).jsonl"
```

After adding this to .bashrc .zshrc or whatever, restart your shell before you fire up your Copilot CLI session. From now on the usage will be logged.

Step 2: Analyze with a tool like tokscale or ccusage:

```bash
bunx tokscale@latest
bunx ccusage@latest daily --breakdown [--since 2026-06-01]
```

(Install bun with brew install bun if needed.)

⚠️ Caveats: These tools track local CLI usage only — web-based usage (code review in PRs, github.com PR chat, etc) is not included. And the cost estimates use public API pricing, which may differ from what one actually pays.

💡 Try this: Run one of the commands above and see what a typical day costs. Most of you will find it's very reasonable — and now you'll know before anyone else tells you.

🔗 https://docs.github.com/en/copilot/reference/copilot-billing/models-and-pricing  
🔗 https://github.blog/news-insights/company-news/github-copilot-is-moving-to-usage-based-billing/  
🔗 https://github.com/ryoppippi/ccusage  
🔗 https://github.com/junhoyeo/tokscale

Are you tracking your AI tool use costs?  

---

🟢 Yes, I monitor usage regularly  
🟡 Vaguely aware but haven't checked numbers  
🔴 Had no idea it was metered now  
⚪ Someone else handles billing, so not my problem :-)

Surprised by any costs? Share what you found!