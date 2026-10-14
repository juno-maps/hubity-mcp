# Hubity

[![Hubity MCP connector: tool definition quality and endpoint health on Glama](https://glama.ai/mcp/connectors/io.hubity/hubity/badges/score.svg)](https://glama.ai/mcp/connectors/io.hubity/hubity)

Month-end billing for consulting, architecture and engineering firms: your AI assistant previews each invoice from approved time, retainers and progress billing, then drafts them for your review.

Hubity runs projects, time, billing and utilization for consulting, architecture, engineering and agency firms. Connect your AI assistant to Hubity and ask in plain words, and the answer comes from your own records, including your past proposals and your firm's knowledge base.

This repository holds the public documentation and registry entry for Hubity's hosted MCP server. The server itself runs at Hubity; there is nothing to install.

## Connect

| | |
|---|---|
| Server URL | `https://hubity.io/api/mcp` |
| Transport | Streamable HTTP (remote) |
| Sign-in | OAuth 2.1 with PKCE, with a Hubity consent screen |
| Registry name | `io.hubity/hubity` |

Add `https://hubity.io/api/mcp` as a custom connector in any assistant that supports remote MCP servers, sign in to Hubity, and approve the connection. Step-by-step setup for each assistant: https://hubity.io/integrations/mcp

You need a Hubity account. What you can see follows your role in Hubity.

## Bill the month

Ask your assistant to bill last month and it shows you each invoice first: approved time, expenses, the retainer fee and progress billing against the contract, with money held back (retainage) where the project sets it, and anything that needs your decision called out. Confirm, and it drafts them.

Nothing is sent. Every draft is marked as drafted by your assistant and waits in Hubity for a person to review and send it.

## Try

- "Bill last month: show me what each invoice would be first."
- "Which active projects are at risk, and are they profitable?"
- "What is the longest-open unpaid invoice?"
- "What is our WIP for last month?"
- "Who was over capacity last month?"

## Tools

| Tool | What it does | Changes data |
|---|---|---|
| `preview_month_billing` | Previews the month's invoices and the decisions to make | No |
| `create_month_invoice_drafts` | Drafts the previewed invoices for your review; nothing is sent | Yes |
| `get_project_profitability` | Revenue, cost and margin by project | No |
| `get_utilization_report` | Billable and total utilization by person | No |
| `forecast_cash_flow` | Expected cash from open invoices by age, plus the value of unbilled time | No |
| `list_projects` | Projects, or one project in full | No |
| `list_tasks` | Tasks, or one task in full | No |
| `list_staff` | Team members, departments and reporting lines | No |
| `list_meetings` | Meetings, or one meeting in full | No |
| `list_invoices` | Invoices, or one invoice in full | No |
| `list_proposals` | Proposals, or one proposal in full | No |
| `list_deals` | Sales pipeline deals, or one deal in full | No |
| `list_pto_requests` | Time off and leave, including who is out | No |
| `search_knowledge` | Searches the company knowledge base | No |
| `log_time_entry` | Logs a time entry | Yes |
| `create_invoice_from_proposal` | Drafts an invoice from an accepted proposal; nothing is sent | Yes |

## Prompts

Ready-made prompts for firm jobs: `bill_the_month`, `month_end_wip`, `whos_over_capacity`, `projects_losing_money`, `collections`, `standup`, `meeting_prep`, `weekly_report`.

## Permissions and privacy

Reading needs your sign-in and approval and follows your role; drafting invoices or logging time needs write access you approve, and every change is audited.

- You approve each connection on a Hubity consent screen that names the app, shows where it will send you back, and lists what it can do.
- Sensitive documents are left out, private staff details are excluded by role, and data is kept separate per company.
- Your assistant never sends anything to a client. Each change is tied to the person who approved access.
- Disconnect any assistant at any time in Hubity under Integrations.

Privacy policy: https://hubity.io/privacy#ai-assistants
Terms: https://hubity.io/terms

## Find Hubity in

- [Official MCP Registry](https://registry.modelcontextprotocol.io/v0.1/servers?search=io.hubity/hubity) (`io.hubity/hubity`)
- [Glama](https://glama.ai/mcp/connectors/io.hubity/hubity)
- [Smithery](https://smithery.ai/servers/hubity/hubity)
- [MCP.so](https://mcp.so/servers/hubity)

## Learn more

- [Free calculators](https://hubity.io/tools): utilization rate, billing rate and multiplier, fee estimate, and a progress billing template
- [Guides for architecture, engineering and consulting firms](https://hubity.io/guides): go/no-go decisions, pricing a fee, progress billing, WIP, utilization
- [Glossary](https://hubity.io/glossary) of project, proposal and billing terms
- [Compare Hubity](https://hubity.io/compare) with Deltek, BQE CORE, Unanet, Monograph, BigTime, Harvest and others

## Support

- Email: support@hubity.io
- Security reports: security@hubity.io (see [SECURITY.md](SECURITY.md))
- Status: https://hubity.io/status

Hubity is made by Juno Maps. The documentation in this repository is licensed under [CC BY 4.0](LICENSE).
