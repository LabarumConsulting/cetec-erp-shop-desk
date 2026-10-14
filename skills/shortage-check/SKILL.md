---
name: shortage-check
description: Check component shortages for one CETEC work order against bins. Use when the user names a work order, order line, or job and asks what is short. Read-only.
---

# Shortage check

Read-only. Do not adjust quantity on hand, allocate, or receive material in this skill.

## When to use

The user names one work order, order line, or job and wants components short against bins.

## Before you call tools

Confirm the Cetec MCP server is connected. If the user did not name a work order, ask for the order number or line id. Do not guess.

## Workflow

1. Resolve the work order. If several lines match, list them and ask which one.
2. Get the BOM or components still required for that line, including quantity required and quantity issued or picked if the tool returns it.
3. For each component, get quantity on hand and available quantity in bins. Available is on hand minus what is already allocated, when the tool distinguishes them.
4. Short means available quantity is below quantity still required. Still required is required minus issued, when both fields exist. Otherwise compare available to required and say you could not see issued quantity.
5. Ignore components with no part number. Do not treat a missing bin record as zero unless the tool explicitly returned zero.

## Verify

Part numbers and quantities come from tool results only. If a component has no inventory record, say "no bin record" rather than "zero on hand."

## Return

The work order, part, and customer. Then the short rows: component, required, issued if known, available, short by. If nothing is short, say that and list the components you checked. End with the tool calls you used.
