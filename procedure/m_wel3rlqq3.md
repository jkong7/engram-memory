---
id: "m_wel3rlqq3"
kind: "procedure"
scope: "project:~/dev/chartside"
title: "Chartside GCP permission grant script"
tags: ["deploy","gcp","permissions"]
importance: 5
trust: "extracted"
status: "active"
created: "2026-10-08T02:09:18.305Z"
updated: "2026-10-08T02:09:18.305Z"
source: "claude-code claude-code:f89b8479-212c-4c74-ba0d-2de8115ddb0e"
---

# Chartside GCP permission grant script

The agent's auto-mode permissions block Chartside's deploy/gcp-grant.sh, so Jonny runs it in-session with the ! prefix: ! cd ~/dev/chartside && sh deploy/gcp-grant.sh. It creates the chartside-run service account, grants that account read access to Chartside's six secrets, and creates a private data bucket. If the first grant fails right after the account is created, wait about 30 seconds and rerun; the script skips steps that already exist.
