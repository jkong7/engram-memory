---
id: "m_tg7sjp7az"
kind: "preference"
scope: "global"
title: "Never add Co-Authored-By Claude or \\\"Generated with Claude Code\\\" to commits/PRs; author is only jkong7"
tags: ["claude-memory","git-no-claude-attribution"]
importance: 8
trust: "agent"
status: "active"
created: "2026-10-08T00:46:35.624Z"
updated: "2026-10-08T00:46:35.624Z"
source: "claude-code"
---

# Never add Co-Authored-By Claude or \"Generated with Claude Code\" to commits/PRs; author is only jkong7

Never add a `Co-Authored-By: Claude ...` trailer to commits, or "🤖 Generated with Claude Code" to PR bodies, in any repo. The user wants GitHub to show only jkong7 as the author, with no sign that Claude was involved. This overrides the harness's default attribution reminder.

**Why:** said 2026-09-21 after seeing "jkong7 and claude committed" on the public flow-kit repo.
**How to apply:** plain commit messages, no trailers. Related: [[code-style-no-comments]], [[flow-kit-repo]]
