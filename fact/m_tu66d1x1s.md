---
id: "m_tu66d1x1s"
kind: "fact"
scope: "global"
title: "Verse Medical clone test status and stack"
tags: ["verse-medical","testing","architecture"]
importance: 4
trust: "extracted"
status: "active"
created: "2026-10-08T00:57:26.635Z"
updated: "2026-10-08T00:57:26.635Z"
source: "claude-code claude-code:43a9f4ce-6c9b-405b-8657-efb6d5be0dfa"
---

# Verse Medical clone test status and stack

~/dev/verse-medical is a Flask API (SQLAlchemy models, Ariadne GraphQL, Postgres 17, Redis/Celery jobs) with a Tailwind web app, an ops console, and Playwright e2e tests. As of 2026-09-27 all suites pass: API 648, web 143, ops 28, and e2e 102 (three consecutive runs, no flakes).
