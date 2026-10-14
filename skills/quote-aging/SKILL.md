---
name: quote-aging
description: Age open CETEC quotes. Use when the user asks which quotes are sitting, stale, or dead, or wants open quotes by age. Read-only.
---

# Quote aging

Read-only. Do not convert a quote to an order and do not create a quote in this skill.

## When to use

The user wants open quotes by age, with no recent activity, customer and part named.

## Before you call tools

Confirm the Cetec MCP server is connected. If it is not, stop and point them at `https://{instance}.cetecerp.com/goapis/mcp`. Do not ask for the token in chat.

## Workflow

1. List open quotes. Include created date, last activity or revision date, customer, and line parts if the tool returns them.
2. Age is days from the quote date, or from last activity if that field exists, to today. Use the field you actually received. Say which field you aged on.
3. Group into under 7 days, 7 to 30, and over 30. A quote is sitting when it is open and the age field is over 14 days with no newer activity. Do not call a quote dead unless the user uses that word or the status is already lost or closed.
4. Sort the sitting group oldest first.

## Verify

Do not invent a customer, part, or date. If the list is truncated, say the limit and how to narrow it (customer, age, owner).

## Return

A table or tight list: quote id, customer, part, age in days, last activity, status. Then a one-line count per age bucket. End with the tool calls you used.
