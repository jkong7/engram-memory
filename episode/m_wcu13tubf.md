---
id: "m_wcu13tubf"
kind: "episode"
scope: "global"
title: "Local Ollama server on the spare Mac"
tags: ["claude-code"]
importance: 3
trust: "extracted"
status: "active"
created: "2026-10-10T21:19:01.244Z"
updated: "2026-10-10T22:25:49.356Z"
source: "claude-code claude-code:ef2ef60d-a958-4a18-b5fb-1f452f6675ca"
---

# Local Ollama server on the spare Mac

Jonny set up the spare MacBook as an Ollama server reachable over Tailscale. The menu bar app ignored the launchctl host setting, so the server was started manually bound to the Tailscale IP, and a call from the main Mac succeeded. The assistant then tested qwen3.5:9b with Burner's real Lena prompt. The model needed reasoning turned off and produced weak results on the dense prompt. Jonny is weighing cheaper hosted models for Burner, citing cost, and nothing was decided.
