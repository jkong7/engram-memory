---
id: "m_zyrdk10ik"
kind: "procedure"
scope: "global"
title: "Starting blackbox so prism shows run history"
tags: ["blackbox","prism"]
importance: 4
trust: "extracted"
status: "active"
created: "2026-10-08T03:48:58.465Z"
updated: "2026-10-08T03:48:58.465Z"
source: "claude-code claude-code:a7c69623-88f0-4d50-9f5b-3f8b4f20f09a"
---

# Starting blackbox so prism shows run history

blackbox is not a background service, so prism's 'History from blackbox' list stays empty until it runs. Start it with `node src/cli.ts serve` from ~/dev/blackbox.
