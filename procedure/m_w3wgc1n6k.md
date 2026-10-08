---
id: "m_w3wgc1n6k"
kind: "procedure"
scope: "global"
title: "Remove Claude co-author trailers from repo history"
tags: ["git","attribution"]
importance: 3
trust: "extracted"
status: "active"
created: "2026-10-08T02:00:59.807Z"
updated: "2026-10-08T02:00:59.807Z"
source: "claude-code claude-code:e5283869-7611-45a2-9d5d-9c9afbecd75f"
---

# Remove Claude co-author trailers from repo history

Use git filter-branch -f with --msg-filter and a python one-liner that drops lines starting with 'Co-Authored-By: Claude', run over -- --all, then git push --force origin main. Commit IDs change. The agent's permission system blocked the force-push, so Jonny ran it himself.
