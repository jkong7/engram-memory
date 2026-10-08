---
id: "m_tg7wx3d5n"
kind: "preference"
scope: "global"
title: "Standing routine since 2026-10-04 - fill Instinct's blocked application packets from ~/dev/jobsearch/handoffs/ in Jonny…"
tags: ["claude-memory","instinct-handoff-packets"]
importance: 8
trust: "agent"
status: "active"
created: "2026-10-08T00:46:35.769Z"
updated: "2026-10-08T00:46:35.769Z"
source: "claude-code"
---

# Standing routine since 2026-10-04 - fill Instinct's blocked application packets from ~/dev/jobsearch/handoffs/ in Jonny…

Standing routine (Jonny, 2026-10-04): whenever triage runs (or Jonny says "handoffs"), `git -C ~/dev/jobsearch pull` and check `handoffs/` for packets from [[instinct-agent]].

For each packet in `handoffs/` (not `handoffs/done/`):
1. Open the application link in a new Chrome tab (Claude in Chrome, his real session), sign in if the packet says an account exists.
2. Complete the remaining steps exactly as written and upload the resume it names, through the final review screen. **Never click Submit.**
3. Tell Jonny it is ready to submit, and append `Status: review-ready` (plus tab/link) at the bottom of the packet. Leave it in `handoffs/`.
4. Only after Jonny says it went through: append the outcome and confirmation number, move it to `handoffs/done/`.
5. If blocked (captcha, missing answer), append what is needed from Jonny at the bottom and leave it in `handoffs/`.

Never invent answers beyond the packet; use [[frq-answer-bank]] only if the packet points there.

**Why:** Instinct's cloud browser gets datacenter-flagged; his Mac has a home IP and real cookies. Jonny explicitly kept stop-before-Submit for handoffs (2026-10-04): he taps Submit himself.

**How to apply:** same rules as any application: [[browser-one-tab-per-application]] (new tab, stop before Submit, about 5 at a time), [[one-application-per-company]] blocklist check first, captcha walls go to Jonny.
