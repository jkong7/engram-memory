---
id: "m_wnpge1lok"
kind: "fact"
scope: "project:~/dev/burner"
title: "Burner AI routing"
tags: ["burner","ai","routing"]
importance: 6
trust: "extracted"
status: "active"
created: "2026-10-08T02:16:23.880Z"
updated: "2026-10-08T02:16:23.880Z"
source: "claude-code claude-code:0f0c7d7c-5437-4647-a798-12dfd23816e3"
---

# Burner AI routing

Burner routes live conversations (texts, calls, date scenes, character creation) to Claude, configured in ~/dev/burner/.env.local with BURNER_LLM=claude. Background chatter (group chats, feed comments, likes, Ping crowd replies) runs on local qwen3:14b via Ollama. Photos use Gemini.
