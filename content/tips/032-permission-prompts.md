---
title: "Tip #32: Tired of the permission prompts?"
date: 2026-04-27
categories: ["Agents"]
weight: 32
summary: "Most tools let you auto-approve agent actions. Three caveats: you lose checkpoints, verbal rules vanish, and you must set permissions correctly."
---

"Allow file read?" Yes. "Allow bash command?" Yes. "Allow write?" Yes yes yes. If you use an AI coding agent, you know the drill. The constant permission prompts break your flow — and most people just approve everything anyway.

Most tools now offer a way to skip the prompts. Claude Code has "auto mode" — a second AI reviews each action against a safety policy. OpenCode has a build mode that applies changes without confirmation. The details differ, but the question is the same: should you let the agent run?

Mostly yes(?) — with three caveats:

**You lose your checkpoints.** Those prompts were annoying, but they forced you to see what the agent was about to do. Without them, it's easy to go fully passive — and that's how comprehension debt builds ([Tip #29](/ai-for-coding/tips/029-comprehension-debt/)). Mitigation: review the plan before you let it execute, and read the diff before you commit.

**"Verbal" rules vanish.** If you say "don't touch the database," that works until context compaction removes it. Put boundaries in config files or instruction files instead — they're permanent. (Also: make sure it cannot reach the PROD base, please 🙏.)

**You must set the permissions correctly.** Auto-approve without proper limits is just `--dangerously-skip-permissions` 💀 with extra steps. Review what's allowed and blocked. Restrict writes to your project directory. Block force-pushes to protected branches. The defaults are reasonable — but they don't know your infrastructure.

💡 **Tip:** Whatever tool you use, find its permission settings and make a deliberate choice. The worst option is clicking "yes" 200 times without reading.

---

**How do you handle agent permissions?**

🟢 Auto-approve with safety rules configured  
🟡 I approve each action manually  
🔴 I skip all permission checks  
⚪ I hadn't thought about it

What's your setup? 🧵