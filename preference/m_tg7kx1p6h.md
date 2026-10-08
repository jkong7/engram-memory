---
id: "m_tg7kx1p6h"
kind: "preference"
scope: "global"
title: "Ashby forms - selections can look filled but not commit; Jonathan hit \\\"required\\\" prompts on Submit for fields already…"
tags: ["claude-memory","ashby-fill-verify","applications","forms","ashby"]
importance: 8
trust: "agent"
status: "active"
created: "2026-10-08T00:46:35.339Z"
updated: "2026-10-08T03:15:30.088Z"
source: "claude-code"
---

# Ashby forms - selections can look filled but not commit; Jonathan hit \"required\" prompts on Submit for fields already…

On Ashby forms, a field can display a value that never committed, so on Submit Jonathan gets asked to fill something "already done". Seen 2026-10-06 on Normal's State/Country of Residence combobox (my Illinois pick showed, then had to be redone).

**Why:** Jonathan: "make sure ... that the clicks are final im pressing submit but then its asking me to fill out something i already did".

Confirmed 2026-10-06 on Niantic Spatial: clicks and typing aimed at element refs (find/ref) silently did nothing for text fields and Ashby Yes/No buttons (only radios took). Coordinate clicks from a fresh screenshot, then typing, worked every time.

**How to apply:** get each field's screen position (JS getBoundingClientRect scaled to the screenshot frame, or a fresh screenshot), click there, type, and re-read values after blur. Don't trust ref-based clicks for text or Yes/No buttons. for location/autocomplete comboboxes, type, wait for the option list, click the option with a real coordinate click on a fresh screenshot, then blur and re-read the input to confirm the value stayed. Date pickers: pick the day in the calendar (JS-set dates land one day early). Before marking a tab "Ready to submit", re-read every required field after blur. Related: [[react-select-fill-technique]], [[browser-one-tab-per-application]]
