---
id: "m_wg1nn1qza"
kind: "episode"
scope: "global"
title: "Chartside core slice"
tags: ["claude-code"]
importance: 3
trust: "extracted"
status: "active"
created: "2026-10-08T02:10:26.400Z"
updated: "2026-10-08T02:10:26.400Z"
source: "claude-code claude-code:77f132c3-5975-485f-b08a-c34c1d1510d4"
---

# Chartside core slice

Jonny asked what Chartside's pitch is against Heidi, Suki, Abridge and DAX, then had the assistant explain the phone-line architecture (Twilio as plumbing, Deepgram for speech, Claude or the offline engine for notes). He then asked for a thin core slice of the app, with the hook workflow and SOAP notes only and everything else hidden behind a flag. The work was done on branch core/slice in a worktree, with all 192 full-edition tests and 79 core tests passing, and nothing pushed or merged. A local core build was started at localhost:3160.
