---
id: "m_tg7ligzhe"
kind: "preference"
scope: "global"
title: "Every job application gets its own fresh Chrome tab; never navigate an existing application tab to a new form"
tags: ["claude-memory","browser-one-tab-per-application"]
importance: 8
trust: "agent"
status: "active"
created: "2026-10-08T00:46:35.362Z"
updated: "2026-10-08T00:46:35.362Z"
source: "claude-code"
---

# Every job application gets its own fresh Chrome tab; never navigate an existing application tab to a new form

When filling job applications in Chrome, open a **new tab for every single application** via `tabs_create_mcp`. Never reuse or navigate an existing application tab to a different form.

**Why:** Navigating a filled tab to the next form destroys the previous fill with no warning. This happened once mid-batch: eleven applications were filled by reusing a single tab, and only the last two survived. Jonathan caught it ("im not seeing the 11 tabs?? i only see 2??") and all eleven had to be re-filled. He restated the rule twice, so treat it as absolute.

**How to apply:** one `tabs_create_mcp` call per role, then `navigate` that new tabId, then fill. Leave every filled tab open and stopped before Submit so Jonathan can review and submit each one himself. Expect 10 to 20 open tabs during a batch; that is the intended end state, not clutter.

Related: [[jobsearch-pipeline]]

**Update 2026-09-30:** Tab count limit. Jonathan said "Chill out, close some of the tabs. The RAM is going crazy" after 27 Workday/Oracle sign-in tabs were opened at once. Open forms in small waves (about 5 new tabs at a time), fill them, and open the next wave only after he submits or closes some. Never pre-open a whole batch of sign-in pages.
