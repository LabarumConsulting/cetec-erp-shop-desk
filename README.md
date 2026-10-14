# CETEC Shop Desk by Labarum Consulting

Read-only shop questions against your own Cetec MCP. The plugin does not ship a Cetec connection and it does not contain a token. You point the bot at your instance and keep the credential in that bot's secrets, not in this repo and not in chat.

Labarum Consulting is a Cetec ERP Service and Integration partner. This pack is not an official Cetec product, and it is not endorsed by xAI, Anthropic, or OpenAI.

Cetec: https://cetecerp.com
Labarum: https://labarumconsulting.com
Inquiries: hello@labarumconsulting.com

## What you get

Twenty playbooks. A shop can also ask about any data their own Cetec MCP returns. If a tool cannot answer or cannot join two records, the skill stops. That is a pass.

- **Floor brief.** Late work, shortages on those jobs, open NCRs, what can ship.
- **Week commit.** Orders due in five days that are short or stuck.
- **Quote aging.** Open quotes by age, no recent activity.
- **Shortage check.** One work order, components short against bins.
- **Buyer brief.** Open POs past due, by vendor, and the job they block.
- **Receiving today.** PO lines due today or overdue, and the job waiting.
- **Outside process.** Plating, heat treat, weld-out, or other vendor POs holding a job.
- **Capacity this week.** Load by work center for the next five days.
- **Customer desk.** Open orders, open quotes, and AR for one customer.
- **Credit before ship.** Past-due invoices against an order in shipping. Does not hold it.
- **Part check.** On hand, on order, and demand for one part.
- **Where used.** BOMs and open work orders that consume one part.
- **Invoice aging.** Open invoices by age, customer named.
- **Ready to invoice.** Finished or shipping jobs with no invoice.
- **Promise date.** Can a date be promised, given material and this week's capacity.
- **Stuck in location.** Jobs that have not moved, even if they are not late.
- **NCR by customer.** Open and recent NCRs for one customer.
- **Repeat NCR.** Parts with more than one open or recent NCR.
- **Quotes ready.** Sitting quotes not blocked on material or capacity. Does not convert.
- **Job packet.** One work order and the records around it.

## Read and write

This pack refuses writes. Cetec's MCP still exposes write tools, including create quote, create BOM, and update BOM. A skill cannot turn those tools off. Do not say yes to a write. Writes have no undo.

Out of this pack: creating a quote or BOM, moving a work order, adjusting quantity on hand, receiving a PO, converting a quote, creating an invoice, holding an order. Those stay a person in Cetec.

## Connect your shop

1. In Cetec, open Admin, APIs and More, MCP, and confirm MCP is enabled.
2. Endpoint. Live: `https://{instance}.cetecerp.com/goapis/mcp`. Test: `https://{instance}.cetecerpbeta.com/goapis/mcp`.
3. Token. The Admin JSON API token from Admin, Configuration is the credential this MCP has accepted. Or, after oauth token enabled is checked on a user, create a script token from My Profile, Tokens, and use the Access Token. That Access Token is tied to the user, only works on `/goapis` endpoints, and expires in 72 hours. Do not use the Refresh Token. Do not use an API Client id or client secret.

Store the token as a secret on the bot, not in chat and not in this repo. Cetec's first 1,000 API calls a month are free. After that, Cetec bills the instance. Cetec documents this MCP server as experimental.

This plugin is free to install.

## Local install

Symlink this repo into `~/.cursor/plugins/local/cetec-shop-desk` and reload, or install from the marketplace once the listing is public. The marketplace only lists public repos.
