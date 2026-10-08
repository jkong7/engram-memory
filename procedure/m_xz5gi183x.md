---
id: "m_xz5gi183x"
kind: "procedure"
scope: "global"
title: "Filling job application forms in Chrome: dropdowns, uploads, autocomplete"
tags: ["job-search","browser","procedure"]
importance: 4
trust: "extracted"
status: "active"
created: "2026-10-08T02:53:17.353Z"
updated: "2026-10-08T02:53:17.353Z"
source: "claude-code claude-code:fabe3a0a-bbb8-408b-a791-9e015b730f8e"
---

# Filling job application forms in Chrome: dropdowns, uploads, autocomplete

Lessons from filling job forms in Jonathan's Chrome (2026-10-06). Greenhouse, Ashby, Workday and Workable dropdowns only open while the Chrome window is visible. Hidden or background tabs skip rendering the menus and throttle timers, which stalls scripts. In a visible window, focus the dropdown with JS and send a real ArrowDown key, or click by element reference. Synthetic events alone did not open these menus. SmartRecruiters renders its form in shadow DOM, so the resume upload tool cannot reach the input. Add a temporary file input to the page, upload into it, then pass that file to the shadow-DOM resume input. Address City fields need a real-keystroke autocomplete pick. Ashby can show a value that never committed, so verify on the review screen before Submit.
