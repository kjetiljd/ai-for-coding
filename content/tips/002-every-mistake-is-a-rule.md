---
title: "Tip #2: Every AI mistake is a rule"
date: 2026-02-20
categories: ["Instruction Files"]
weight: 2
summary: ""
---

Copilot just generated code that ignores your team's conventions. You sigh, fix it manually, move on.

The advice out there is: Don't.
Use that moment as a gift. Open `.github/copilot-instructions.md` and add one line:

Never use Optional.get() without isPresent() check or consider orElse(null).

Or:

Avoid SpringBoot-tests when unit tests will suffice.

Result: Copilot is less likely to make that mistake again.

This is a habit loop that separates teams that fight AI from teams that train it. One practitioner at a workshop a couple of weeks ago described writing so much context for AI that he got a finger injury — because the labor had shifted from coding to writing constraints. That's an extreme, but the direction is right.

DORA 2025 calls these files "an important source of team norms and practices." Think of your instruction file as a living document: it starts thin, and grows every time AI surprises you.

💡 Try this: Next time Copilot generates something wrong, add the rule before you fix the code.

🔗 [Tip #1](/ai-for-coding/tips/001/)


---

How often do you update your instruction file(s)?  

🟢 Regularly — it's part of our workflow  
🟡 Sometimes, when I remember  
🔴 I have one but haven't updated it  
⚪ Starting from scratch after this tip