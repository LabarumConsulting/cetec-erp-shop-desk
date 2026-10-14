---
name: ready-to-invoice
description: Finished or shipping CETEC jobs with no invoice. Use when the user asks what can be billed. Read-only.
---

# Ready to invoice

Use the shop's own Cetec MCP. Do not invent jobs. Do not create an invoice.

## When to use

- "What can we bill?"
- Finished or shipping jobs with no invoice.

## Steps

1. List jobs in a finished or shipping location.
2. If a tool can show whether an invoice exists for that job, drop the ones already invoiced.
3. If status and invoices cannot be joined, say so and stop.
4. Do not create an invoice.

## Return

Job, customer, part, location. If the join is missing, stop.
