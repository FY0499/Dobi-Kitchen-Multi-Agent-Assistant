# Dobi Kitchen Multi-Agent Assistant

An n8n multi-agent assistant I built for a food business. Customers send their requests through Telegram, and the main agent directs each request to the right flow for orders, cancellations, or delivery questions.

<img width="579" height="237" alt="Dobi Kitchen workflow demo" src="https://github.com/user-attachments/assets/4b7d1bdb-9965-48cd-b76e-4543a3fdc642" />

## How it works

1. A customer sends a message through Telegram.
2. The main agent identifies what the customer needs.
3. The request is directed to the relevant order, cancellation, or delivery agent.
4. Connected tools handle the required information and follow-up.
5. The workflow sends a response through Telegram.

## Main features

- Multi-agent routing and task handling.
- Order, cancellation, and delivery support.
- Telegram messaging.
- Google Sheets and Gmail integrations.
- Webhook connection for workflow integration.

## Technologies

n8n, AI Agents, Google Gemini, Telegram, Google Sheets, Gmail, and Webhooks.

## Setup

Import [workflow.json](./workflow.json) into n8n, add your credentials, connect the required Google Sheets and Telegram details, and test the workflow using your own data.
