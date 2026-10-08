---
id: "m_w03e11fqf"
kind: "procedure"
scope: "project:~/dev/resume"
title: "Build LaTeX resume with Tectonic"
tags: ["latex","resume","tooling"]
importance: 3
trust: "extracted"
status: "active"
created: "2026-10-08T01:58:02.170Z"
updated: "2026-10-08T01:58:02.170Z"
source: "codex codex:01a0c08c-5773-72e3-a9e4-87a55e73513d"
---

# Build LaTeX resume with Tectonic

Build the resume with Tectonic (XeTeX). Wrap \input{glyphtounicode} and \pdfgentounicode=1 in \ifdefined guards, since they are pdfTeX-only primitives and error under XeTeX. Tectonic 0.17 rejects --keep-logs=false, so remove that flag from the Makefile. Verify by diffing pdftotext output and rendering PNG previews against the original PDF, and confirm the page count is one.
