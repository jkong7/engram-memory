---
id: "m_wjvwoe5wi"
kind: "procedure"
scope: "global"
title: "Driving Raycast UI from scripts"
tags: ["raycast","automation","gotchas"]
importance: 3
trust: "extracted"
status: "active"
created: "2026-10-08T02:13:25.650Z"
updated: "2026-10-08T02:13:25.650Z"
source: "claude-code claude-code:2e52f474-abe7-4b05-bfdc-980e18f1d2f5"
---

# Driving Raycast UI from scripts

Keystroke automation of Raycast was unreliable: modifiers dropped and ⌘N did not create a note. Accessibility clicks worked better. Raycast hides when it loses focus, which kills running commands, so post-capture steps need a detached background process.
