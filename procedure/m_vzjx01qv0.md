---
id: "m_vzjx01qv0"
kind: "procedure"
scope: "global"
title: "Making a new Raycast app appear in Raycast"
tags: ["raycast","macos","gotcha"]
importance: 4
trust: "extracted"
status: "active"
created: "2026-10-08T01:57:36.983Z"
updated: "2026-10-08T01:57:36.983Z"
source: "codex codex:01a0c08c-5772-76f2-9c8d-aa3c5a0e71a7"
---

# Making a new Raycast app appear in Raycast

Raycast indexes apps only at launch. After creating or rebuilding an app bundle in /Applications, restart Raycast with killall Raycast, then open -a Raycast. Then assign the hotkey in Settings > Applications. Registering the bundle with lsregister also helps.
