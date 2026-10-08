---
id: "m_tv1yb3yeu"
kind: "episode"
scope: "global"
title: "Technician-job pairing problem (2026-09-28)"
tags: ["claude-code"]
importance: 3
trust: "extracted"
status: "active"
created: "2026-10-08T00:58:07.718Z"
updated: "2026-10-08T00:58:07.718Z"
source: "claude-code claude-code:8ec62443-b31e-4691-8c6a-20514b6fb4fb"
---

# Technician-job pairing problem (2026-09-28)

Jonny pasted a technician-to-job matching problem using Manhattan reach. The assistant proposed rotating coordinates (u = x + y, v = x - y) so each reach becomes a square, then a merge-sort segment tree for the range queries. Jonny asked for spelled-out names and less polished code, and the assistant rewrote it with a recursive segment tree and verified it against brute force. Jonny then asked for a summary of the algorithm and why coordinates are rotated first. He pasted his own buggy version, and the assistant identified 7 bugs (wrong append call, undefined `tree`/`v_node`, mismatched loop variable, wrong `positions` key, `teach_v` typo, wrong function name, missing import) and gave corrected lines.
