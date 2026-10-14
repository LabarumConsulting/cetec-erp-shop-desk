---
name: credit-before-ship
description: Past-due invoices against a CETEC order in shipping. Use when the user asks if this order should leave for a customer. Does not hold the order.
---

# Credit before ship

Use the shop's own Cetec MCP. Do not invent balances. Do not hold an order.

## When to use

- "Should this order leave for {customer}?"
- Past-due invoices against an order in shipping.

## Steps

1. Resolve the order. If it is not in shipping or finished, say so and stop.
2. List open invoices for that customer. Keep past-due ones.
3. Name the oldest invoice and the past-due amount if the tool returns them.
4. Do not hold the order. Do not take a payment.

## Return

Order, customer, past-due amount if known, oldest invoice. If AR was not returned, say so.
