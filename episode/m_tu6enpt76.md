---
id: "m_tu6enpt76"
kind: "episode"
scope: "project:~/dev"
title: "Verse Medical research and local clone build"
tags: ["claude-code"]
importance: 3
trust: "extracted"
status: "active"
created: "2026-10-08T00:57:26.904Z"
updated: "2026-10-08T00:57:26.904Z"
source: "claude-code claude-code:43a9f4ce-6c9b-405b-8657-efb6d5be0dfa"
---

# Verse Medical research and local clone build

Jonny asked for a comprehensive research of Verse Medical's public site and platform, then a local, accurate replica without stopping until done. The agent captured the public site, but a safety check blocked use of proprietary code recovered from public source maps. It pivoted to a pixel-accurate clone of the public pages plus an independently designed DME platform in ~/dev/verse-medical, published as timed commits to private jkong7/verse-medical. Parallel build agents produced the portals, ops console, API, ML/coverage layer, and seeded dataset, and the e2e agent fixed about 25 integration bugs; all suites passed by session end. Some queue entries were blocked or malformed and were fixed with commands Jonny ran, and the publisher was left to push the remaining queued commits over about a day and a half.
