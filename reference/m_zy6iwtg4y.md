---
id: "m_zy6iwtg4y"
kind: "reference"
scope: "global"
title: "Pushback repo and publisher"
tags: ["pushback","publishing","github"]
importance: 5
trust: "extracted"
status: "active"
created: "2026-10-08T03:48:31.349Z"
updated: "2026-10-08T03:48:31.349Z"
source: "claude-code claude-code:86ba8e22-d8fe-4156-9f0a-cc2b17bcb738"
---

# Pushback repo and publisher

jkong7/pushback is the public GitHub repo for Pushback (~/dev/pushback), created 2026-10-08. A launchd agent, com.jkong7.pushback-publisher, pushes its 29 queued commits one at a time with random 10 to 90 minute gaps. Log: ~/Library/Logs/pushback-publisher.log. Stop with: touch ~/dev/pushback/.git/publish/stop.
