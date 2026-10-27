# Dobi Kitchen Multi-Agent Assistant

An n8n multi-agent assistant for a food business, designed to route customer messages to order, cancellation, and delivery-related actions.

## Setup
1. Import the sanitized workflow JSON into n8n when it is added to this repository.
2. Reconnect AI, messaging, and data-store credentials in n8n.
3. Configure the menu, order handling, and delivery tools for your own business.
4. Test each route with sample conversations before production use.

## Security
Never commit credentials, webhook URLs, customer records, or private IDs. End-to-end testing is not confirmed.

## Project status
This README documents the project scope and setup expectations. Add the sanitized workflow export before attempting import, then validate it in your own n8n instance.