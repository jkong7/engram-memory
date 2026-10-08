---
id: "m_wjvv12mom"
kind: "procedure"
scope: "global"
title: "Give zsh Full Disk Access for iCloud sync jobs"
tags: ["macos","icloud","permissions"]
importance: 5
trust: "extracted"
status: "active"
created: "2026-10-08T02:13:25.547Z"
updated: "2026-10-08T02:13:25.547Z"
source: "claude-code claude-code:2e52f474-abe7-4b05-bfdc-980e18f1d2f5"
---

# Give zsh Full Disk Access for iCloud sync jobs

Background zsh jobs cannot read iCloud Drive and fail with 'Operation not permitted' until /bin/zsh is granted Full Disk Access. Add it in System Settings → Privacy & Security → Full Disk Access by pressing + then ⌘⇧G, typing /bin/zsh, and enabling the toggle.
