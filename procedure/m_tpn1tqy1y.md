---
id: "m_tpn1tqy1y"
kind: "procedure"
scope: "global"
title: "Gitignore Go binary names without hiding cmd dirs"
tags: ["git","gitignore","go"]
importance: 3
trust: "extracted"
status: "active"
created: "2026-10-08T00:53:55.265Z"
updated: "2026-10-08T00:53:55.265Z"
source: "claude-code claude-code:252b8c72-8dca-4799-b5c1-9ea1b891b24e"
---

# Gitignore Go binary names without hiding cmd dirs

In a Go repo's .gitignore, anchor binary names with a leading slash (for example /sidebet). An unanchored name also matches cmd/<name> directories and silently ignores their source code.
