# Local Data And Privacy

KeyRing AI is designed as a local-first desktop application. Normal AI prompts and responses are sent from the user's machine directly to the selected AI provider using the user's provider key. KeyRing AI's website layer supports account, license, download, and update workflows. It is not a prompt relay for everyday model use.

## What Local-First Means

Local-first means the desktop app keeps workspace state on the user's device and gives the user direct control over provider keys, model selection, attachments, history, exports, metrics, prompt presets, and workflow settings.

Local-first does not mean no data leaves the device. When the user sends a prompt to a selected provider, that provider receives the prompt and any selected context, attachments, tool inputs, or generated workflow data included in the request.

## Local Data Categories

The desktop app can maintain local records for conversations, attachments, generated media, text-to-speech assets, exports, metrics, provider configuration, model configuration, and internal app state needed to operate the local workspace.

These records make the product useful: users can reload history, export work, compare providers, inspect metrics, and keep reusable presets. They also mean users should treat the local app data area as sensitive if their prompts, attachments, or outputs are sensitive.

## Provider Data Responsibility

Each provider has its own terms for API usage, retention, training, logging, safety review, regional handling, billing, and deletion. KeyRing AI helps users route requests, but it does not override provider policies.

Before sending confidential, regulated, or customer data to any provider, confirm that the provider and model are approved for that use case.

## Website Data Boundary

The KeyRing AI website handles commercial workflows such as account access, license state, downloads, and updates. It does not need normal prompt or response content to perform those functions.

This separation is intentional. The website establishes product entitlement and distribution trust. The desktop app handles the user's AI work locally and communicates directly with selected providers.

## Exports And Sharing

Exports can contain prompts, model responses, metadata, provider names, model names, token counts, costs, attachment references, tool traces, or generated output. Review exports before sharing them with teammates, support, or public channels.

Do not share exports that contain credentials, private customer information, confidential business data, or provider output that should remain internal.

## Public Boundary

This document describes the public privacy model. It does not include private storage paths, database schema, encryption implementation details, source code, customer data, or security-sensitive internals.
