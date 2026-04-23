---
title: "Tip #30: Give your agent all the repos at once"
date: 2026-04-23
categories: ["Workflow Patterns"]
weight: 30
summary: "Clone related repos into one parent folder, add an AGENTS.md, and start your agent there. It lazy-loads on demand — cross-system understanding with no extra token cost."
---

Your agent usually only sees what's in its working directory. If you're building a frontend that talks to a backend API in another repo, the agent might be guessing at contracts, inventing endpoints and hallucinating types.

The fix is old-school: the meta-repo pattern. Clone related repos into one parent folder and start the agent there. Agents lazy-load files on demand, so having five repos available doesn't cost more tokens until it actually reads something. But when it needs to check an API contract or a shared type, it can.

```
my-project/
├── frontend/        ← your repo
├── backend-api/     ← their repo
├── shared-models/   ← the contract
└── AGENTS.md        ← "frontend calls backend via /api/v2, see shared-models for types"
```

The upgrade that makes it work: add an AGENTS.md in the parent folder describing how the repos relate. That makes the agent architecturally aware, not just file-aware. A colleague uses this for her daily work and reports implementations that are "definitely up to spec."

💡 Try this: mkdir my-meta-repo && cd  && git clone <repo1> && git clone <repo2> — then start your agent from my-meta-repo. Add an AGENTS.md describing the relationships.
🔗 [Meta-repo workshop (pre-AI)](https://kjetiljd.github.io/meta-repo-workshop/)

---

**How many repos does your agent usually see?**

🟢 Just one — the repo I'm working in  
🟡 Two or more — I've grouped some related ones  
🔴 I use a monorepo, so everything's in one place already  
⚪ I hadn't thought about this, have to try it!

Got a multi-repo setup that works? Share it in 🧵