---
id: "m_xyocu1dba"
kind: "procedure"
scope: "global"
title: "ATS form gotchas: Paylocity, SmartRecruiters, Breezy, Ashby, Greenhouse"
tags: ["automation","forms","ats"]
importance: 5
trust: "extracted"
status: "active"
created: "2026-10-08T02:52:55.244Z"
updated: "2026-10-08T02:52:55.244Z"
source: "claude-code claude-code:cf1fc1d0-8f84-4aea-8d4a-128a4430cb8f"
---

# ATS form gotchas: Paylocity, SmartRecruiters, Breezy, Ashby, Greenhouse

Paylocity state dropdowns take the abbreviation ("IL"), since typing "Illinois" finds nothing. Its reference and prior-employment questions are required comboboxes, so set them with clicks. SmartRecruiters renders in shadow DOM, so locate the file input directly; the upload can throw an error yet still register, so confirm the filename under Resume. Breezy restores drafts, so check the DOM before retrying. When refs go stale, switch to coordinate clicks. On Ashby, type text fields for real and click dropdowns by coordinates. On Greenhouse, set text with the native setter and dropdowns with real clicks, and confirm async school lookups before pressing Enter. Workday needs a sign-in, and Built In hides employer links behind a login.
