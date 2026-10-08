---
id: "m_welcq1wjr"
kind: "episode"
scope: "global"
title: "Chartside overnight Wave 2 and live replacement"
tags: ["claude-code"]
importance: 3
trust: "extracted"
status: "active"
created: "2026-10-08T02:09:18.644Z"
updated: "2026-10-08T02:09:18.644Z"
source: "claude-code claude-code:f89b8479-212c-4c74-ba0d-2de8115ddb0e"
---

# Chartside overnight Wave 2 and live replacement

Jonny asked for new Chartside ideas and features with full permissions. The assistant ran four research tracks, built four features on separate branches with worktree builders, merged them into interface/wave2, and ran four security reviews that found and fixed six authentication and access problems, all tested with real Claude and Deepgram keys. On 2026-09-30 Jonny approved replacing the live Cloud Run site with wave2, keeping chartside-00002-h4c as the rollback target, and all branches were pushed to GitHub with main fast-forwarded to match.
