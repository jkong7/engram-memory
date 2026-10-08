---
id: "m_w2dlm14cq"
kind: "procedure"
scope: "global"
title: "Bulk unsubscribe via Gmail Manage subscriptions"
tags: ["gmail","automation","unsubscribe"]
importance: 3
trust: "extracted"
status: "active"
created: "2026-10-08T01:59:48.699Z"
updated: "2026-10-08T01:59:48.699Z"
source: "claude-code claude-code:2e655855-48c3-43e4-8533-010568616811"
---

# Bulk unsubscribe via Gmail Manage subscriptions

Gmail's Manage subscriptions page offers one-click Unsubscribe per sender. Rows shift as senders are removed, so target each sender by address, not by screen position. A hidden tooltip can capture clicks meant for the real button, so inspect the button markup first. Some senders (LeetCode, Snapchat, Quora) open a different dialog. Reload the page to clear leftover dialogs. Long click loops can exceed a 45-second tool limit but keep running in the page, so check back before rerunning.
