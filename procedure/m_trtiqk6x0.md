---
id: "m_trtiqk6x0"
kind: "procedure"
scope: "global"
title: "Reading and moving Apple Notes with AppleScript"
tags: ["apple-notes","applescript","macos","gotcha"]
importance: 5
trust: "extracted"
status: "active"
created: "2026-10-08T00:55:36.896Z"
updated: "2026-10-08T00:55:36.896Z"
source: "claude-code claude-code:26594fc5-11f7-435a-b2db-c0364f5641a8"
---

# Reading and moving Apple Notes with AppleScript

Terminal already has Notes permission, so osascript can read and write Apple Notes. Note bodies come back as simple HTML. Writing over notes with checklists, tables, drawings or attachments can strip them, so append instead. Moving an audio-only note with AppleScript sends it to Recently Deleted; restore it in the Notes app. `lists` is a reserved word, so don't use it as a variable name.
