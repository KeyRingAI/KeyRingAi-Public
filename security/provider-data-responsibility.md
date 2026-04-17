# Provider Data Responsibility

KeyRing AI lets users work with multiple AI providers from one local desktop workspace. The user brings their own provider accounts and provider API keys. That model gives users control, but it also means provider data responsibility remains important.

## Direct Provider Relationship

For normal AI requests, KeyRing AI sends selected prompts and context from the user's desktop environment to the selected provider. The provider receives the data included in the request and handles it under that provider's API terms, privacy policy, retention rules, billing model, and safety systems.

KeyRing AI does not change those provider terms. Before sending sensitive data, customers should confirm that the selected provider, model, region, account settings, and use case are approved for that data.

## Data That May Be Sent

Depending on the workflow, a provider request may include prompt text, system context, selected attachments, tool inputs, generated workflow context, model configuration, or conversation history needed for continuity.

If a user includes an attachment or routes a Chatroom or Roundtable workflow to multiple providers, each selected provider may receive the relevant context for its role.

## Customer Controls

Customers should use provider-side spending limits, usage alerts, data-retention settings, scoped keys, and organizational controls where available. They should also review KeyRing AI local history, exports, attachments, and presets for sensitive material.

Do not assume a provider can receive regulated, confidential, or customer data just because a key works. Provider readiness and data-governance readiness are separate decisions.

## Reporting Concerns

If you believe KeyRing AI routed data in a way that conflicts with the product's documented behavior, report it privately with the provider, workflow, model, visible settings, and a sanitized reproduction. Do not include secrets or customer data in public issues.

## Public Boundary

This document describes public responsibility boundaries. It does not include private provider adapters, source code, request internals, customer data, or security-sensitive implementation details.
