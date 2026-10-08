---
id: "m_wdeyn1g29"
kind: "procedure"
scope: "global"
title: "Filling job application forms in Chrome"
tags: ["job-search","procedure","browser"]
importance: 5
trust: "extracted"
status: "active"
created: "2026-10-08T02:08:23.611Z"
updated: "2026-10-08T02:08:23.611Z"
source: "claude-code claude-code:6f90aeb8-7ed1-40ae-be37-f4b27d5654f0"
---

# Filling job application forms in Chrome

Steps and gotchas for filling application forms through Chrome automation:
1. Keep the Chrome window visible and not minimized. Hidden or minimized tabs stop the job site's scripts, so dropdown selections don't save and waits time out.
2. Attach files (resume, cover letter, transcript) only after the page has fully loaded. Otherwise the upload is ignored.
3. Check the form for re-rendering after a resume parse. If the form resets, re-check the fields before continuing.
4. Stop before Submit. Leave consent boxes, SMS consent, family-related questions and e-signatures for Jonny.
5. Sign-in or account creation pages (Workday, Oracle, iCIMS, Intuit Register) are Jonny's to complete. Tell him and wait.
6. Oracle forms send an email verification code when applying.
7. If a posting shows 'page doesn't exist', check whether it has closed before retrying.
