---
name: stuck-in-location
description: CETEC work orders sitting in one location past a threshold, even if they are not late yet. Use when the user asks what is stuck or not moving.
---

# Stuck in location

Use the shop's own Cetec MCP. Do not invent locations or days. Do not move a work order.

## When to use

- "What is stuck?"
- Jobs that have not moved, separate from jobs that are already late.

## Steps

1. List open work orders with current location and time in that location.
2. Keep the ones past the threshold the user named. If they did not name one, use three working days and say that is the default.
3. Separate these from jobs that are already past due.
4. Do not move anything.

## Return

Work order, part, location, days in location. If the tool does not return time in location, say so.
