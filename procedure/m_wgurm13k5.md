---
id: "m_wgurm13k5"
kind: "procedure"
scope: "global"
title: "Verifying Greenhouse and Ashby form answers register before Submit"
tags: ["job-search","chrome","automation","greenhouse","ashby","lever"]
importance: 6
trust: "extracted"
status: "active"
created: "2026-10-08T02:11:04.135Z"
updated: "2026-10-08T02:11:04.135Z"
source: "claude-code claude-code:534e4112-9c0a-4f69-93c2-43bfa7985ac4"
---

# Verifying Greenhouse and Ashby form answers register before Submit

Scripts that only set a field's displayed value often leave the form's internal state blank, so Submit reports required fields as empty. Greenhouse: set dropdowns by real click, typing the option and pressing Enter, or call the field's onChange with the option value. Ashby: answers save only on focusout, so a plain blur event is not enough. Use the form's own handlers, one field at a time. Lever forms are plain HTML, so script values stick, but location autocomplete needs a suggestion picked. Verify each field against the form's saved state, not the screen. Background tabs throttle timers, so check state directly or work in the foreground.
