---
title: "Tip #26: Before you wire AI agents to CI/CD, read this"
date: 2026-04-17
categories: ["Security"]
weight: 26
summary: "The Clinejection attack showed how a malicious PR description can hijack an AI agent with CI/CD access. Know the risk before you automate."
---

In March, the  AI coding extension Cline had a real supply chain compromise. Not because the AI wrote bad code — because an AI agent had too many permissions and processed untrusted input.

Here's what happened: Cline ran a Claude-powered bot on their public GitHub repo that auto-triaged new issues. Someone opened an issue with a crafted title that tricked the bot into running npm install for a malicious package. The package's preinstall script poisoned the GitHub Actions cache — which the release workflow also used. Result: a compromised version of Cline was published to npm for ~8 hours and installed by 4,000+ developers.

The vulnerability wasn't the AI model. It was architecture:
— The triage bot had Bash and Write access. It only needed Read.
— The triage and release workflows shared a cache key.
— Issue titles went straight into the prompt with no sanitization.

If you're connecting AI agents to workflows triggered by external input (issues, PRs, webhooks), think about what they can reach. An issue triage bot that can write to the release cache is a supply chain risk.

💡 Takeaway: Aim to give AI agents the minimum permissions they need. Separate trust boundaries between external-facing and release workflows.
🔗 The original Clinejection writeup by Adnan Khan — the full attack chain, step by step  
🔗 Snyk's analysis of the attack

---

**How is AI connected to your CI/CD pipelines?**

🟢 We have AI-triggered workflows (code review, triage, etc.)  
🟡 We're considering it  
🔴 Not yet — AI stays on the developer's machine  
⚪ Not yet - and hadn't thought about the security angle

Reflections on AI + CI/CD security?