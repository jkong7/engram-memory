---
id: "m_yqqia1my7"
kind: "fact"
scope: "global"
title: "qwen3.5:9b falls short on Burner's dense prompt"
tags: ["burner","local-models","qwen"]
importance: 4
trust: "extracted"
status: "active"
created: "2026-10-10T22:25:49.147Z"
updated: "2026-10-10T22:25:49.147Z"
source: "claude-code claude-code:ef2ef60d-a958-4a18-b5fb-1f452f6675ca"
---

# qwen3.5:9b falls short on Burner's dense prompt

In a 2026-10-10 test, qwen3.5:9b on the spare drafted a Lena text reply through Burner's real prompt builder. It broke several formatting rules, reused a phrase the prompt said to avoid, and misread the situation. Context was not the problem: the 5,601-token prompt fit the 8,192 limit.
