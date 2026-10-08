---
id: "m_03upd5be4"
kind: "fact"
scope: "project:~/dev/burner"
title: "Burner LLM routing"
tags: ["burner","llm","config"]
importance: 6
trust: "extracted"
status: "active"
created: "2026-10-08T03:52:56.048Z"
updated: "2026-10-08T03:52:56.048Z"
source: "claude-code claude-code:0bb7a16a-53c8-46ba-b08e-d35e2c974114"
---

# Burner LLM routing

Burner's live and background LLM calls are routed by ~/dev/burner/llm.json, which is set to provider gemini as of 2026-10-08 and overrides BURNER_LLM=claude in .env.local. Photos also use Gemini.
