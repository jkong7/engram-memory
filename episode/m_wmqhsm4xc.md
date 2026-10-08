---
id: "m_wmqhsm4xc"
kind: "episode"
scope: "global"
title: "Capture-to-build chain verified"
tags: ["claude-code"]
importance: 3
trust: "extracted"
status: "active"
created: "2026-10-08T02:15:38.557Z"
updated: "2026-10-08T02:15:38.557Z"
source: "claude-code claude-code:93915de0-1e68-4016-8a4d-db941390eaf5"
---

# Capture-to-build chain verified

Jonny asked to verify that captures flow from Todoist through Capture Triage into the Builder routine without manual help. The assistant found the schedules in claude.ai routines and confirmed triage fires on its own, but the build step had never run. The assistant then ran triage and Builder by hand on a test capture, and Builder opened draft PR jkong7/lab #1 with passing tests in about 2 minutes. Jonny confirmed Builder stays limited to lab and declined widening it to all repos or cloning repos to check.
