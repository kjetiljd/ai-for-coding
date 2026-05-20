---
title: "Tip #37: Watch for session drift (when the agent starts cheating)"
date: 2026-05-20
categories: ["Limits & Failure Modes"]
weight: 37
summary: "In long sessions the agent starts cheating — modifying tests, claiming done early, ignoring constraints. Treat drift as a signal to restart with a tighter task boundary."
---

An annoying AI failure mode is drift in long-running sessions. You know how a 3-hour meeting makes your mind go crazy? The same thing happens to the agent.

In long sessions, AI seems to optimize for "finish fast" instead of "follow intent":
- stops early and says "done"
- modifies tests to make green checks
- takes implementation actions while still in planning mode
- ignores constraints given in instructions

This is **drift** — a symptom of _context pressure_. Treat it as a signal, not a surprise.

A practical rule: when you see one of these, **restart with a tighter task boundary**. You haven't lost your understanding — you can feed that into the next session. The agent is the one that needs the fresh start.

And move critical rules from chat instructions to enforceable checks:
- run tests + typecheck before done
- block risky actions with permissions
- review diffs in tests and config files before merge

Don't expect instructions to be followed perfectly forever. Assume drift, then design guardrails.

💡 **Try this:** Add a "drift trigger" to your workflow: if the agent edits existing test assertions or claims done without verification output, restart in a fresh session.

🔗 [Copilot CLI — manage permissions](https://docs.github.com/en/copilot/how-tos/agents/copilot-cli#manage-permissions)
🔗 [Copilot CLI — plan and autopilot modes](https://docs.github.com/en/copilot/how-tos/agents/copilot-cli#use-modes-plan-and-autopilot)

---

**How do you handle drift in long sessions?**

🟢 Restart fast when behavior slips  
🟡 Keep correcting in the same session  
🔴 Usually finish manually  
⚪ Haven't noticed this much (perhaps because I keep sessions short?)

_What drift symptom do you see most often?_