---
id: "m_y82vs1khe"
kind: "fact"
scope: "global"
title: "Caffeinate toggle on ⌘⇧O"
tags: ["shortcuts","macos","caffeinate"]
importance: 4
trust: "extracted"
status: "active"
created: "2026-10-08T03:00:14.001Z"
updated: "2026-10-08T03:00:14.001Z"
source: "claude-code claude-code:565412f1-9aeb-4489-9f5b-2b3527ac890f"
---

# Caffeinate toggle on ⌘⇧O

As of 2026-10-05, Jonny's caffeinate toggle is bound to ⌘⇧O in ~/.config/skhd/skhdrc. It runs ~/.local/bin/caffeinate-toggle, which starts caffeinate -d detached, stores its PID in ~/.cache/caffeinate-toggle.pid, and posts an on/off notification. This is separate from the Raycast caffeinate script.
