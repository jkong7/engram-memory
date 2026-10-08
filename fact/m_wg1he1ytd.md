---
id: "m_wg1he1ytd"
kind: "fact"
scope: "project:~/dev/chartside"
title: "Chartside core edition location and switch"
tags: ["chartside","edition","git"]
importance: 6
trust: "extracted"
status: "active"
created: "2026-10-08T02:10:26.218Z"
updated: "2026-10-08T02:10:26.218Z"
source: "claude-code claude-code:77f132c3-5975-485f-b08a-c34c1d1510d4"
---

# Chartside core edition location and switch

Chartside's core edition is on branch core/slice (6 commits on main, not pushed or merged as of 2026-10-01) in worktree ~/dev/chartside-wt/core. CHARTSIDE_EDITION defaults to core; set it to full to restore the complete app without rebuilding. Hidden areas are listed in src/lib/edition.ts.
