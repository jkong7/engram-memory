---
id: "m_y6jeh1lw1"
kind: "procedure"
scope: "project:~/dev/burner"
title: "Generating Burner character photos with Nano Banana"
tags: ["burner","images","nano-banana","vertex"]
importance: 5
trust: "extracted"
status: "active"
created: "2026-10-08T02:59:02.032Z"
updated: "2026-10-08T02:59:02.032Z"
source: "claude-code claude-code:1f5a085b-bd97-4878-8653-44e4af7a0e80"
---

# Generating Burner character photos with Nano Banana

1. Pass one of Jonny's photos as a style reference, with the instruction to match its polish but never its person.
2. Add one concrete beauty line per character to the prompt. Wording alone did not make Nano Banana idealize faces.
3. Shoot posed, curated shots for profiles and feed. Keep stories and selfies casual.
4. Drop the film-grain and color-shift phone treatment. Resize with a clean JPEG at high quality instead.
5. Run at most about 3 parallel workers. Five workers hit Vertex 429 rate limits on Nano Banana Pro, and a stale gcloud token caused 401s that required restarting the run.
Backups of the previous photo set go in scripts/.v2 and .v3.
