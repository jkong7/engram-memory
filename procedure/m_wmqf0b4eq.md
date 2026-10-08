---
id: "m_wmqf0b4eq"
kind: "procedure"
scope: "global"
title: "Test the capture-to-PR chain by hand"
tags: ["automation","testing","builder","todoist"]
importance: 4
trust: "extracted"
status: "active"
created: "2026-10-08T02:15:38.433Z"
updated: "2026-10-08T02:15:38.433Z"
source: "claude-code claude-code:93915de0-1e68-4016-8a4d-db941390eaf5"
---

# Test the capture-to-PR chain by hand

1) Add a capture to the Todoist Inbox worded as the Shortcut sends it. 2) Run the Capture Triage routine now instead of waiting: it creates a build-labeled task in Projects and closes the Inbox item. 3) Run the Builder routine: it codes on a branch in jkong7/lab, opens a draft PR, and comments the link on the task. 4) Clone the branch and check the code yourself. On 2026-10-05 this took about 2 minutes end to end (PR jkong7/lab #1).
