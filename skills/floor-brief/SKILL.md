---
name: floor-brief
description: Morning CETEC shop-floor brief. Use when the user asks what is late, what is short, what can ship, or for a stand-up on open work orders and NCRs. Read-only.
---

# Floor brief

Read-only. Never create, move, or adjust a record in this skill.

## When to use

The user wants the state of the floor: late work orders, shortages on those jobs, open NCRs, and what can ship today.

## Before you call tools

Confirm the Cetec MCP server is connected. If it is not, stop and tell the user to add `https://{instance}.cetecerp.com/goapis/mcp` and store the Admin token as a secret. Do not ask them to paste the token in chat.

## Workflow

1. List open work orders and current location. Prefer production status if that tool exists.
2. Mark a job late only when the tool result has a promise date, dock date, or due date that is before today, or the user already called it late. Do not invent a date rule the payload does not support.
3. For each late job, check component availability against bins. A shortage is a component whose available quantity is below the quantity still required. If the tool cannot show that, say so.
4. List open NCRs or other open quality records tied to those jobs or to today. Skip this section if the server has no quality tool.
5. What can ship is work that is in a shipping or finished location, or whose remaining operations are done, and that is not on hold. If location names are unclear, list the candidates and say why they might ship.

## Verify

Every order number, part, quantity, and date in the reply must come from a tool result. If a call fails, say which call failed. Do not fill the gap with a plausible number.

## Return

Four short sections: Late, Short, Open NCRs, Can ship today. Name the work order, part, customer, and the date or quantity that made the row. End with the tool calls you used.
