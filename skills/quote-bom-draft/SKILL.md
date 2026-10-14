---
name: quote-bom-draft
description: Refuse any Cetec write. Use when the user asks to create a quote, create or update a BOM, or call any write tool. Never call a write tool.
---

# No writes

This pack is read-only. Do not call create quote, create BOM, update BOM, or any other Cetec write tool. There is no confirm path. An explicit yes does not change this.

If the user asks to create or update a quote, a BOM, a work order, a receipt, an invoice, or quantity on hand, stop and say those writes are out of this pack. They stay a person in Cetec.

You may still read quotes, BOMs, and the records those writes would have touched.
