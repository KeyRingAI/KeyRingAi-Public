# Examples

This folder contains public-safe workflow examples for KeyRing AI. The examples are written for customers, developers, and evaluators who want to understand how to use the product without access to proprietary application source code.

The examples intentionally avoid private implementation details. They should not include application source code, private infrastructure configuration, secrets, environment files, customer data, internal prompts, real provider credentials, or private audit findings.

## Available Examples

- [Evaluation checklist](evaluation-checklist.md) - a structured way to compare providers and models.
- [Provider setup checklist](provider-setup-checklist.md) - a safe bring-your-own-key setup path.
- [Model Discovery checklist](model-discovery-checklist.md) - steps for newly released or newly discovered models.
- [Roundtable workflow](roundtable-workflow.md) - a public-safe multi-provider discussion example.
- [Attachments workflow](attachments-workflow.md) - a minimal context-sharing example.
- [Agent workflow](agent-workflow.md) - a conservative agent setup and tool-consent example.
- [Provider error triage](provider-error-triage.md) - a clean way to narrow provider failures.

## Contribution Boundary

Public examples should use synthetic or public data only. Do not add proprietary app code, copied private documentation, internal routes, deployment details, credentials, private screenshots, customer transcripts, or real provider keys.

## How To Use These Examples

Start with the checklist closest to your task. Keep the first run small and non-sensitive. Confirm that a minimal provider request works before adding attachments, tools, media generation, Roundtable, or agents. Export results only after reviewing them for sensitive content.
