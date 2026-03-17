---
title: "Tip #5: What actually belongs in your instruction file?"
date: 2026-02-26
categories: ["Instruction Files"]
weight: 5
summary: ""
---

Tips [Tip #1](/ai-for-coding/tips/001/) and [Tip #2](/ai-for-coding/tips/002/) covered setting up `copilot-instructions.md` (or `AGENTS.md`) and growing it over time. But can it grow **too much**?

Some early research suggests yes. A couple of recent studies (ICSE JAWs 2026, ETH Zurich) found that auto-generated instruction files — the kind produced by `/init` commands that scan your codebase and describe what they find — actually **hurt** performance slightly while increasing cost. Meanwhile, hand-written files with genuinely non-obvious info ("use `uv` not `pip`", "the auth middleware is fragile — don't refactor it") seemed to help.

It's early days and these are small studies, so take the numbers with a grain of salt. But the intuition rings true: repeating what's already in the code is noise. Telling the AI what it **can't** discover on its own is signal.

A useful filter to try: before adding a rule, ask yourself — would the AI figure this out anyway from the code and tests? If yes, maybe skip it.

💡 Try this: Review your instruction file (or a teammate's). Is anything in there that the AI would learn just by reading the code? Consider trimming it.

🔗 Addy Osmani's write-up with links to both studies: [https://addyosmani.com/blog/agents-md/](https://addyosmani.com/blog/agents-md/)

Tried pruning your instruction file(s)?

---

🟢 Regularly — it's part of our workflow  
🟡 Yes, once or twice  
🔴 Not removed much yet, no  
⚪ Instruction file ... ? ![:wink:](https://a.slack-edge.com/production-standard-emoji-assets/14.0/apple-medium/1f609@2x.png)

_Have you removed something that you then discovered_ **_had_** _to be in there?_ _🧵_