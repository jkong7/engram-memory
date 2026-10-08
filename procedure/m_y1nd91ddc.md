---
id: "m_y1nd91ddc"
kind: "procedure"
scope: "global"
title: "Workday application form gotchas (Chrome automation)"
tags: ["workday","chrome","playbook"]
importance: 5
trust: "extracted"
status: "active"
created: "2026-10-08T02:55:13.942Z"
updated: "2026-10-08T02:55:13.942Z"
source: "claude-code claude-code:48ee7751-c5c5-43c9-8eb4-69be0a81257b"
---

# Workday application form gotchas (Chrome automation)

1. Workday's resume parse splits one employer into several entries and misfills titles and companies, so check My Experience and delete duplicates before moving on. 2. Save and Continue won't advance while the tab is in the background; the user must bring the tab to the front. 3. Type city and address fields with real keystrokes so Workday registers them. 4. Verify checkboxes and dates after clicking, and re-read element refs first, since guessed refs can click the wrong control.
