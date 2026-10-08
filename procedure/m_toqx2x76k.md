---
id: "m_toqx2x76k"
kind: "procedure"
scope: "global"
title: "Filling Greenhouse and Ashby application forms in Chrome (dropdowns and warm-up)"
tags: ["job-search","chrome","greenhouse","ashby","forms","automation"]
importance: 5
trust: "extracted"
status: "active"
created: "2026-10-08T00:53:13.541Z"
updated: "2026-10-08T00:53:13.541Z"
source: "claude-code claude-code:41c09c34-bd8f-4071-8b35-3d47441aa1ba"
---

# Filling Greenhouse and Ashby application forms in Chrome (dropdowns and warm-up)

Procedure learned filling Greenhouse and Ashby forms (2026-09-22). 1) On a fresh tab, take one normal-size screenshot before any click, or the first clicks are swallowed. 2) Plain clicks on dropdown options are unreliable. Focus each combobox from JS, then send a real ArrowDown to open the menu, and type a filter for searchable ones (school, location). School and location work by typing. 3) Some dropdowns miss intermittently, so collect misses into a retry list and re-check every dropdown afterward. 4) Match experience questions by exact label. 'C#' and 'C' collapse when '#' is stripped, which once put the wrong answer on C. 5) Only write into labeled fields. A Backspace or select-all can clear unlabeled fields such as the 'additional context' textarea. 6) Leave demographics, consent checkboxes, and Submit for Jonny.
