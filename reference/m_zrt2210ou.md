---
id: "m_zrt2210ou"
kind: "reference"
scope: "project:~/dev/burner"
title: "Burner live site on Cloud Run"
tags: ["deploy","gcp"]
importance: 6
trust: "extracted"
status: "active"
created: "2026-10-10T22:54:38.714Z"
updated: "2026-10-10T22:54:38.714Z"
source: "claude-code claude-code:e93bf3b6-8bdc-49bd-822e-3c5c15b165e2"
---

# Burner live site on Cloud Run

Burner's live site is https://burner-792894733520.us-central1.run.app, on Cloud Run in project persona-onboarding-jk. A scheduler job calls its background tick every 5 minutes. Max instances is 1 so saves cannot conflict.
