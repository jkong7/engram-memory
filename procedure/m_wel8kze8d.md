---
id: "m_wel8kze8d"
kind: "procedure"
scope: "global"
title: "Launching parallel builder agents in worktrees"
tags: ["agents","worktrees","process"]
importance: 4
trust: "extracted"
status: "active"
created: "2026-10-08T02:09:18.507Z"
updated: "2026-10-08T02:09:18.507Z"
source: "claude-code claude-code:f89b8479-212c-4c74-ba0d-2de8115ddb0e"
---

# Launching parallel builder agents in worktrees

When launching several builder agents in git worktrees, create each worktree yourself at the correct base branch and install dependencies before the agents start. Builders launched without prepared worktrees made no changes for over an hour and ignored redirects, likely stuck on a hidden permission prompt. After relaunching on prepared worktrees, all builders started writing code within minutes, so confirm first file changes within about 20 minutes.
