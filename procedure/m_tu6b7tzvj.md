---
id: "m_tu6b7tzvj"
kind: "procedure"
scope: "project:~/dev"
title: "Queue timed commits for the Verse publisher"
tags: ["verse-medical","publisher","git","gotcha"]
importance: 5
trust: "extracted"
status: "active"
created: "2026-10-08T00:57:26.801Z"
updated: "2026-10-08T00:57:26.801Z"
source: "claude-code claude-code:43a9f4ce-6c9b-405b-8657-efb6d5be0dfa"
---

# Queue timed commits for the Verse publisher

Append entries to ~/dev/.verse-publisher/queue.tsv: one line per commit, the message, a real TAB, then space-separated file paths. Build lines with printf '%s\t%s\n' so tabs survive. Pasting a command into the prompt can turn tabs into spaces; the publisher then reads message words as paths, git stages nothing, and the entry is skipped. Verify tabs before relying on the queue. The publisher commits as jkong7 with a random 20-30 minute gap and ends at a STOP line.
