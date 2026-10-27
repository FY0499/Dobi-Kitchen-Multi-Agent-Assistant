# Dobi Kitchen Multi-Agent Assistant

An **n8n multi-agent workflow** concept for a food business. A router agent interprets incoming customer messages and delegates order, cancellation, and delivery-related requests to specialist agents.

![Workflow overview](./assets/workflow-overview.svg)

## How it works

1. A customer sends a message through Telegram.
2. The router agent identifies the customer's intent.
3. The request is delegated to a specialist agent, such as order handling, cancellation, or delivery support.
4. Configured integrations can store order information and send notifications.

## Repository contents

- `workflow.json` — exported n8n workflow to inspect and import after configuration.
- `assets/workflow-overview.svg` — conceptual overview diagram.

## Setup

1. Import `workflow.json` into your n8n instance.
2. Configure your own Telegram, AI model, Google Sheets, email, and other required credentials in n8n.
3. Replace placeholders such as `YOUR_GOOGLE_SHEET_ID` and `https://YOUR_N8N_HOST/webhook/REPLACE_WITH_WEBHOOK_ID` with values from your own environment.
4. Review every node and tool connection, including any webhook-triggered actions.
5. Test order, cancellation, delivery, and error paths using synthetic data before activating the workflow.

## Security

- The public workflow has had its embedded spreadsheet identifier and webhook URL replaced with placeholders.
- Credentials are not included intentionally; configure them through n8n's credential manager.
- Never commit API keys, bot tokens, active webhook URLs, private spreadsheet IDs, customer records, or real order data.

## Project status and limitations

This repository contains an exported workflow, but **successful end-to-end execution has not been independently verified**. The diagram is conceptual. Before using this in production, verify node compatibility, tool routing, data handling, and every integration in your own n8n instance.

## Tech stack

- n8n
- AI agent and chat model nodes
- Telegram integration
- Google Sheets and email/webhook integrations (requires your own configuration)
