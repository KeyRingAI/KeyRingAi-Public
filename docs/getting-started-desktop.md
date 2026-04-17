# Getting Started With The Desktop App

This guide walks through a practical first session in KeyRing AI. It is written for evaluators, customers, and developers who want to understand the desktop workflow before connecting production provider accounts.

KeyRing AI is a local-first desktop workspace. The user brings their own AI provider keys, chooses which providers and models to use, and sends requests directly from the desktop app to those providers. The KeyRing AI website supports account, license, download, and update workflows. It does not receive normal chat prompts or AI responses.

## Prerequisites

You need an installed copy of KeyRing AI, an active KeyRing AI license, and at least one supported provider account with API access enabled. For voice playback workflows, an optional ElevenLabs key can be configured. For multi-provider workflows such as Roundtable, at least two configured providers are recommended.

Provider availability depends on the provider account. A model appearing in a provider's model list does not guarantee that the account has billing, regional, tier, quota, or beta access to run that model.

## First Launch

On first launch, KeyRing AI guides the user through license activation and provider setup. License activation confirms that the desktop app is allowed to run for the current user and machine. Provider setup lets the user enter one or more provider API keys.

API keys are used from the local desktop app to call the selected provider. Treat those keys like production credentials: create scoped keys where the provider supports them, avoid sharing them in screenshots, rotate them if exposure is suspected, and remove keys that are no longer needed.

## Configure A First Provider

Open API Settings and choose a provider. Enter the provider API key, save the change, and confirm that the provider shows as configured or active. If the provider requires billing activation, model access approval, or a specific account tier, complete those steps in the provider's own dashboard before using the provider in KeyRing AI.

After a provider is configured, open Provider Manager to review the provider's model inventory. If the provider supports discovery, run Model Discovery to fetch available models from the provider. Review the discovered list, save the provider configuration, and confirm that the model appears in the relevant picker.

## Send A First Prompt

Start a new chat. Select one configured provider and model. Enter a short prompt that does not contain sensitive production data. Send the request and watch the provider tab for status, elapsed time, token information, and any provider error.

A good first prompt is simple and easy to judge, such as asking the model to summarize a public article excerpt, convert a short paragraph into bullet points, or explain a concept. This helps separate provider setup problems from prompt complexity.

## Compare Providers

After one provider works, configure a second provider and send the same prompt to both. KeyRing AI's tabbed layout makes it easier to compare tone, structure, speed, and failure modes. If Chatroom mode is enabled, replies can be routed into a unified conversation view so the user can review the exchange as a single transcript.

When comparing providers, remember that model output quality is affected by model choice, account access, request settings, context length, tool availability, and provider-side policies.

## Add Context With Attachments

Open Attachments to add supporting files. Attachments can be scoped globally or to a specific provider/model workflow. Use the lightest ingestion mode that fits the task: metadata or filename only for discovery-style prompts, first lines for quick inspection, and raw content only when the provider actually needs the file contents.

Files included in a provider request may be sent to that provider. Do not attach confidential, regulated, or customer material unless your organization has approved that provider and use case.

## Review History And Metrics

Open History to find prior conversations, load a session, copy output, export selected records, or delete local records that are no longer needed. History is stored locally on the device.

Open Metrics to review request counts, provider/model usage, estimated cost, latency, token counts, and cost states. Metrics are useful for evaluation and budgeting, but they are estimates unless reconciled against provider invoices or provider-side usage reports.

## Recommended First-Hour Checklist

Activate the license. Configure one provider key. Run a simple prompt. Configure a second provider. Run Model Discovery for at least one provider. Review Model Configuration for one model and confirm that unsupported settings are not forced into every request. Add a small non-sensitive attachment and test attachment scoping. Create one prompt preset. Open History and Metrics to confirm local records are visible.

## Public Boundary

This guide intentionally avoids proprietary implementation details, private endpoints, source paths, infrastructure configuration, secrets, and internal security controls. It describes the public product workflow at a level appropriate for customers and developers evaluating KeyRing AI.
