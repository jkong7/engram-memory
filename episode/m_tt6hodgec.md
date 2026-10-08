---
id: "m_tt6hodgec"
kind: "episode"
scope: "project:~/dev"
title: "Chartside: AI clinician scribe research, build, and push (2026-09-27)"
tags: ["claude-code"]
importance: 3
trust: "extracted"
status: "active"
created: "2026-10-08T00:56:40.255Z"
updated: "2026-10-08T00:56:40.255Z"
source: "claude-code claude-code:6be1b352-effb-4cb0-9a51-91fc1cc16c7b"
---

# Chartside: AI clinician scribe research, build, and push (2026-09-27)

Jonny asked for research on the top 10 AI clinician scribes, including UI teardowns, then a full-stack scribe called Chartside built from the best of them with gap-filling features. The session produced sourced research reports, the Chartside app (ambient capture with Deepgram, note drafting, coding, Epic SMART on FHIR, orgs/roles/SSO, and revenue-cycle coding built on official CMS and ICD-10 files), and 36 commits pushed to the private jkong7/chartside repo. Tests passed on SQLite and Postgres, but Deepgram and Epic were verified only against mocks or the public sandbox. The session ended with a local history saved at ~/dev/chartside/.context/HISTORY.md, and open items are a real Deepgram key, Epic client ID registration, and licensed CPT/NCCI data.
