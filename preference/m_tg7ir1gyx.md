---
id: "m_tg7ir1gyx"
kind: "preference"
scope: "global"
title: "Never use em dashes (or spaced hyphens as dashes) in replies, in anything written on Jonathan's behalf, or in AI produc…"
tags: ["claude-memory","no-em-dashes"]
importance: 8
trust: "agent"
status: "active"
created: "2026-10-08T00:46:35.273Z"
updated: "2026-10-10T00:17:21.030Z"
source: "claude-code"
---

# Never use em dashes (or spaced hyphens as dashes) in replies, in anything written on Jonathan's behalf, or in AI produc…

Never use em dashes. This covers replies to Jonathan, text written on his behalf (emails, FRQs, READMEs, outreach), and the output of any AI agent built for him, such as the Persona onboarding agent in [[persona-onboarding-takehome]].

**Why:** Jonathan said on 2026-09-27 that em dashes read as AI-written. For a take-home judged on how natural the agent sounds, that is a direct quality problem.

**How to apply:** Use a comma, a full stop, or a new sentence. Do not swap in an en dash or a hyphen with spaces around it. Hyphens inside words and number ranges are fine. For model output, do not rely on the prompt alone: also filter in code, as `server/src/agent/plainPunctuation.ts` does.
