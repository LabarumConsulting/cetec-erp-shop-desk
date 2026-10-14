---
name: part-check
description: On hand, on order, and demand for one CETEC part. Use when the user names a part and asks if they can promise a date.
---

# Part check

Use the shop's connected Cetec MCP. One part per run. If the user did not name a part, ask. Do not scan inventory.

1. Confirm the part the tool returned.
2. Quantity on hand by bin, if the tool returns bins. Otherwise total on hand, and say bins were not returned.
3. Open purchase orders for that part: vendor, qty open, due date.
4. Open demand: sales orders or work orders that need the part, with qty and due date, if the tool returns them.

Do not tell the user a promise date unless on-hand and open supply cover the demand you actually retrieved. If they do not, say you cannot promise. Do not adjust quantity. This skill is read-only.
