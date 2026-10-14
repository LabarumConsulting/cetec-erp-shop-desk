---
name: promise-date
description: Can a CETEC date be promised, given material and this week's capacity. Use when the user asks if a date is real. Read-only.
---

# Promise date

Use the shop's own Cetec MCP. Do not invent dates or hours. Do not move a job.

## When to use

- "Can we promise {date} on {part}?"
- Material and this week's capacity against one date.

## Steps

1. Check on hand and open POs for the part.
2. Check this week's load on the work center the tool returns for that part.
3. Say yes only if both cover the date. Otherwise name the block.
4. Do not reschedule anything.

## Return

Part, date, material status, capacity status, yes or no.
