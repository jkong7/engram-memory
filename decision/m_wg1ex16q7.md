---
id: "m_wg1ex16q7"
kind: "decision"
scope: "project:~/dev/chartside"
title: "Chartside stripped to core slice"
tags: ["chartside","scope","architecture"]
importance: 7
trust: "extracted"
status: "active"
created: "2026-10-08T02:10:26.130Z"
updated: "2026-10-08T02:10:26.130Z"
source: "claude-code claude-code:77f132c3-5975-485f-b08a-c34c1d1510d4"
---

# Chartside stripped to core slice

Jonny decided on 2026-10-01 to strip Chartside to a thin, fully working core slice for building: the phone, text and /go recorder hook plus a SOAP-only note editor. Everything else is hidden behind a flag, not deleted. **Why:** the full app is very wide (about 233 endpoints) and works against the pitch.
