---
title: "Tip #1: Give Copilot a memory"
date: 2026-02-19
categories: ["Instruction Files"]
weight: 1
summary: ""
---

Every time you start a Copilot session, it knows nothing about your project. Your conventions, your architecture decisions, your "please don't touch that module" — all gone. You repeat yourself. Every. Single. Time.

Fix: create a file called .github/copilot-instructions.md in your repo. Copilot reads it automatically on every interaction — Chat, Agent Tab, code review, CLI. You write it once, and it just works.

What to put in it:
- Language and framework ("This is a Spring Boot 3.x service in Kotlin")
- Architecture boundaries ("Never call the payment module directly")
- Testing strategy ("Use testcontainers for integration tests")
- Common gotchas ("The legacy API returns XML, not JSON")

Keep it short — 30-50 lines beats a 500-line wall of text. Think of it as onboarding notes, but for AI.

💡 Try this: Create `.github/copilot-instructions.md` in one of your repos today. Start with 5 lines. Add a rule every time Copilot gets something wrong.

🔗 Full docs: https://docs.github.com/en/copilot/customizing-copilot/adding-repository-custom-instructions-for-github-copilot (even includes a prompt that can help you create a longer starting point)


---

Does your team have a copilot-instructions.md yet?  

🟢 Yes, and we maintain it  
🟡 Yes, but it's not maintained  
🔴 Nope, not yet  
⚪ We use AGENTS.md / CLAUDE.md instead