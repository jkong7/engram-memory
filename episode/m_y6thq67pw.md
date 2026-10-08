---
id: "m_y6thq67pw"
kind: "episode"
scope: "global"
title: "Local LLM RAM check"
tags: ["claude-code"]
importance: 3
trust: "extracted"
status: "active"
created: "2026-10-08T02:59:15.191Z"
updated: "2026-10-08T02:59:15.191Z"
source: "claude-code claude-code:e3c57361-395d-44fa-8c01-de27c18a44d7"
---

# Local LLM RAM check

Jonny asked whether his local Ollama models were using RAM and how much. The assistant explained that models stay on disk until prompted and unload about 5 minutes after the last use. Jonny ran llama3 in Terminal, which used roughly 5 GB of unified memory, shown in Wired Memory rather than the per-process column. Running `ollama stop llama3` freed it, and typing /bye alone did not.
