---
id: "m_y5pe0fnty"
kind: "episode"
scope: "global"
title: "Cue build and publisher setup"
tags: ["claude-code"]
importance: 3
trust: "extracted"
status: "active"
created: "2026-10-08T02:58:23.012Z"
updated: "2026-10-08T02:58:23.012Z"
source: "claude-code claude-code:f44417fd-b49b-44ce-9eab-ff7322d77b46"
---

# Cue build and publisher setup

Jonny asked for a long unattended run: research 10 SF AI startups, pick one, research it deeply, and build an improved local version. The agent chose Cluely's category and built Cue in ~/dev/cue, which passes 17 tests and runs end to end in offline rehearsal mode only, since real keys were unreadable. It queued 21 commits and set up a launchd publisher that pushes them to a private GitHub repo with random gaps. Jonny then asked a second Claude Code session (dev-74) to run the same loop in a different consumer AI lane, and a brief was sent to it.
