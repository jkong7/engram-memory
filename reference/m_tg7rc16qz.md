---
id: "m_tg7rc16qz"
kind: "reference"
scope: "global"
title: "DoorDash + Chipotle orders are done via Claude in Chrome using Jonathan's existing logged-in sessions"
tags: ["claude-memory","food-ordering-chrome"]
importance: 6
trust: "agent"
status: "active"
created: "2026-10-08T00:46:35.581Z"
updated: "2026-10-08T00:46:35.581Z"
source: "claude-code"
---

# DoorDash + Chipotle orders are done via Claude in Chrome using Jonathan's existing logged-in sessions

DoorDash (doordash.com) and Chipotle (chipotle.com) have no connector; order through Claude in Chrome. Both were logged in as Jonathan in Chrome as of 2026-09-21. DoorDash default address: Extended Stay America Suites – Milwaukee – Brookfield. Chipotle is set to "Deliver to Home". Past DoorDash orders: Wingstop, Popeyes, Walgreens, Chipotle, CVS.

**Why:** User wants Claude to place food orders on their behalf.
**How to apply:** Build the cart, then show the items, total, address, and payment method, and get an explicit yes before tapping Place Order. Never type in a password or card number. If a session has expired, ask the user to log in again.
