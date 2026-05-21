---
title: "Tip #38: Talk to your agent"
date: 2026-05-21
categories: ["Workflow Patterns"]
weight: 38
summary: "Voice dictation isn't for dictating code — it's for the prose around code that agents need. Speaking is 3× faster than typing, and the reduced friction produces richer prompts."
---

_Agents take over code generation. What grows in its place? The prose around code — context docs, instructions, architecture decisions. That's a typing-bound task, but voice can unblock it._

Voice dictation isn't for dictating code. It's for the rich context that agents actually need: explaining intent, describing constraints, iterating on design. Speaking is about 3× faster than typing, and when input is cheap you naturally give the model more to work with.

A few patterns that work:

- **Voice your long prompts, type your short ones.** Surgical one-liners are fine to type. But when you need to explain context, constraints, and intent — just say it.
- **Two humans discuss, AI listens.** Have a design conversation with a colleague while AI synthesizes structure from the transcript.
- **Pair voice with a screenshot.** Drag in an image for grounding, speak for intent. High-leverage combo.

The catch: there's an awkward-phase barrier. Five minutes isn't a fair trial — it takes sustained use before the workflow clicks. And voice is for prompts, not for `camelCaseIdentifiers`.

**Tools to try:** macOS built-in dictation (Fn twice) works for a first test. For better accuracy, [Handy](https://github.com/cjpais/Handy) is open-source, runs Whisper locally, and works across apps — choose whisper-large-v3 for Norwegian. (Wispr Flow is a polished commercial option but sends audio to some cloud.)

💡 Try this: next time you need to explain a non-trivial task to the agent, press the dictation key (Fn twice on Mac) instead of typing. See if the prompt comes out richer.
🔗 [Peter Steinberger — "Just Talk To It"](https://steipete.me/posts/2025/just-talk-to-it-the-no-bs-way-of-agentic-engineering/)

---

**How do you give input to your coding agent?**

🟢 Voice regularly — for prompts and context  
🟡 I've tried voice but dropped it  
🔴 Typing only — I'm fast enough  
⚪ Hadn't considered using voice

_What's your biggest barrier to using voice for coding work?_