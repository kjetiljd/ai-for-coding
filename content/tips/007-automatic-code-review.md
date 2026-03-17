---
title: "Tip #7: Let Copilot review every PR — automatically"
date: 2026-03-06
categories: ["Getting Started with GitHub Copilot"]
weight: 7
summary: ""
---

You can set up GitHub Copilot to automatically review your pull requests. You need a branch ruleset: go to your repo's Settings → Rules → Rulesets, create a new branch ruleset, and check "Automatically request Copilot code review." Pick which branches to target (default branch, all branches, or a pattern).
[]()
Two options worth knowing about:
- Review new pushes — Copilot re-reviews on each push, not just the first one
- Review draft PRs — catch issues before you even mark the PR as ready

Don't want to go all-in yet? You can also invoke Copilot as a reviewer manually on any PR — just add "Copilot" as a reviewer from the Reviewers menu.

The review uses full project context and leaves comments with suggested fixes you can apply in a couple of clicks. Copilot always leaves a "Comment" — never "Request changes" — so it won't block your merge. It's a first pass, not a gatekeeper.

The DNA team (Finland) have made this mandatory on all PRs — freeing human reviewers to focus on architecture and logic rather than the basics.

💡 Try this: Pick one repo and enable automatic Copilot review on e.g feature branches. See what it catches on the next few PRs.

🔗 Setup guide: Configuring Automatic Code Review for a Single Repository


---

**What is your experience with Github Copilot code reviews?**

🟢 We have already set up automatic reviews  
🟡 We are invoking Copilot as a reviewer on a case by case basis  
🔴 We haven't looked at this yet  
⚪ This is not applicable to our work

Tried this already? What's been your experience — useful signal or just noise?