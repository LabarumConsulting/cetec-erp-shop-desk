---
name: job-packet
description: All CETEC details for one work order. Use when the user names a job and wants the packet, the traveler, or everything on that order. Read-only. One work order per run.
---

# Job packet

Read-only. Do not move the job, adjust quantity, or create an NCR.

## Before you query

Confirm the Cetec MCP is connected. If they did not give a work order id, ask. One job per run. Do not scan the open order book.

## What to pull

Only what the tools return. Leave a line blank rather than invent it.

1. Header: work order, part, revision if returned, qty ordered, qty complete, customer, promise or dock date, current location, days in that location.
2. Components: part, qty required, qty short against bins. Name an open PO and its due date only if the tool returned it.
3. Quality: open NCRs on this job or this part, id and status. Skip closed ones unless they ask.
4. Outside: if the current location is a processor, or a PO is holding the job off site, name the vendor and days out. If the tool cannot say, skip the line.
5. Status: can ship only if the location is finished or shipping, nothing is short, and no NCR is open. Otherwise say what is blocking it.

If the work order id does not resolve, stop. Do not pick a similar job.

## Answer shape

A short header, then shortages, then NCRs, then the one-line block. This is the card someone walks to the machine with. Floor brief is the whole shop. This is one job.
