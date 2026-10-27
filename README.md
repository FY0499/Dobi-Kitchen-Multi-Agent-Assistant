# Dobi Kitchen Multi-Agent Assistant

An **AI-powered multi-agent workflow concept built with n8n** for handling common customer requests for a food business. The workflow is designed around a router agent that identifies customer intent and delegates requests to specialist agents for order support, cancellations, and delivery questions.

> **Project status:** Portfolio prototype. The exported workflow has not been independently verified end to end. Review and test every node and integration in your own n8n instance before using it with real customers or orders.

![Workflow overview](./assets/workflow-overview.svg)

## Problem

Food businesses often receive repetitive messages about placing orders, cancelling requests, and checking delivery details. Handling these manually can create delays and inconsistent responses.

## Proposed solution

This project explores a multi-agent pattern in which a router interprets a Telegram message and passes the request to a relevant specialist agent. Configured integrations can support storing order information and sending follow-up notifications.

## Workflow architecture

1. **Customer message** — a customer sends a request through Telegram.
2. **Intent routing** — a router agent interprets the message and selects a suitable request path.
3. **Specialist handling** — the workflow is designed to route order, cancellation, and delivery requests to dedicated handling paths.
4. **Connected tools** — configured integrations may read or write order information and send notifications.
5. **Response and follow-up** — the workflow can be adapted to return a response or escalate cases that need human attention.

## Key concepts demonstrated

- Multi-agent workflow design and task delegation
- Intent-based routing for customer support
- Telegram as a conversational entry point
- Workflow integration concepts using Google Sheets, email, and webhooks
- Credential configuration and safe handling of deployment-specific values

## Tech stack

- **n8n** — workflow orchestration
- **AI agent / chat model nodes** — intent interpretation and request handling
- **Telegram** — customer messaging interface
- **Google Sheets, email, and webhooks** — optional integrations that require your own configuration

## Repository contents

- `workflow.json` — exported n8n workflow to inspect and import after configuration.
- `assets/workflow-overview.svg` — conceptual workflow diagram.

## Setup

1. Import `workflow.json` into your n8n instance.
2. Configure your own Telegram, AI model, Google Sheets, email, and other required credentials using n8n's credential manager.
3. Replace placeholders such as `YOUR_GOOGLE_SHEET_ID` and `https://YOUR_N8N_HOST/webhook/REPLACE_WITH_WEBHOOK_ID` with values from your environment.
4. Inspect each node, agent prompt, tool connection, and webhook-triggered action. Adjust any node parameters for your installed n8n version.
5. Test order, cancellation, delivery, invalid input, and error-handling paths with synthetic data.
6. Keep the workflow inactive until you have verified the expected behavior and security settings.

## Security and responsible use

- Credentials are intentionally not provided; configure them in n8n's credential manager.
- Do not commit API keys, Telegram bot tokens, active webhook URLs, private spreadsheet IDs, customer records, or real order data.
- Use synthetic test data during development.
- Add validation, logging, error handling, and human escalation before considering production use.

## Current limitations

- End-to-end execution has not been independently verified.
- The diagram describes the intended architecture; it does not prove every route is operational.
- Integrations require credentials and environment-specific configuration.
- Agent outputs and order-related actions need testing and appropriate safeguards before real-world use.

## Potential next steps

- Add explicit human handoff for uncertain or sensitive requests.
- Validate required order fields before taking action.
- Improve retry and error-handling paths.
- Add test cases for each intent and document verified results.
- Include a short demo recording after a working end-to-end run has been confirmed.

---

Built as a practical portfolio project exploring **AI agents, multi-agent orchestration, and workflow automation with n8n**.
