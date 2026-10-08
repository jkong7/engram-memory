---
id: "m_tp45ua67a"
kind: "procedure"
scope: "global"
title: "Collecting Instagram Reels data from the logged-in Chrome session"
tags: ["instagram","reels","scraping","chrome","browser-automation"]
importance: 5
trust: "extracted"
status: "active"
created: "2026-10-08T00:53:30.721Z"
updated: "2026-10-08T00:53:30.721Z"
source: "claude-code claude-code:967a0dc1-e678-43aa-bf02-34c67280927a"
---

# Collecting Instagram Reels data from the logged-in Chrome session

Instagram Reels videos only play and the feed only loads more while the Chrome window is visible and in front. In a hidden or minimized window, players stay black, playback pauses, and the feed stalls after about 5 reels. Check window visibility before a collection run. Instagram's internal web endpoints (the feed discover endpoint and comment endpoints) return reels, captions, stats and full comment threads using the logged-in session, which is faster than clicking. Page output may be too large for JS return values, so render the dump into the page and read it as text. Navigation clears injected helper functions, so re-inline them on each page. Audio for transcription can be saved from the page, but files should be packed and downloaded in one archive. Transcribe locally with faster-whisper after installing ffmpeg.
