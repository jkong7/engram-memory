---
id: "m_yqqdcej08"
kind: "procedure"
scope: "global"
title: "Serve Ollama on the spare Mac over Tailscale only"
tags: ["ollama","local-models","tailscale","macos"]
importance: 7
trust: "extracted"
status: "active"
created: "2026-10-10T22:25:48.845Z"
updated: "2026-10-10T22:25:48.845Z"
source: "claude-code claude-code:ef2ef60d-a958-4a18-b5fb-1f452f6675ca"
---

# Serve Ollama on the spare Mac over Tailscale only

The Ollama menu bar app ignores the launchctl OLLAMA_HOST setting and listens on localhost, so Jonny starts the server by hand. Steps on the spare: 1) Quit Ollama from the llama menu bar icon. 2) In Terminal run: OLLAMA_HOST=100.111.166.56:11434 OLLAMA_CONTEXT_LENGTH=8192 OLLAMA_KEEP_ALIVE=-1 ollama serve. 3) Leave that window open. If the port is in use, the app is still running, so quit it and rerun. Binding to the Tailscale IP keeps it off campus Wi-Fi, unlike the 'Expose Ollama to the network' toggle. Gotchas: the server stops when the window closes or the machine reboots, and the spare drops off Tailscale when it sleeps, so run 'sudo pmset -a sleep 0 disablesleep 1' with the lid open and charger plugged in.
