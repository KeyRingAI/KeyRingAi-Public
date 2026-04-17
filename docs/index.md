# KeyRing AI Public Documentation

This folder contains public-facing KeyRing AI documentation for customers, developers, and evaluators. It explains product behavior, onboarding, provider setup, architecture, and trust boundaries without exposing proprietary application source code.

## Start Here

- [Quickstart](quickstart.md) - install, activate, connect one provider, and send a first prompt.
- [Getting Started](getting-started.md) - fuller onboarding path for license, install, provider keys, first use, attachments, and Model Discovery.
- [Provider API Keys](provider-api-keys.md) - bring-your-own-key setup, provider readiness, and key hygiene.
- [Workflow Examples](../examples/README.md) - concrete public workflows for provider setup, comparison, Model Discovery, reasoning models, attachments, and troubleshooting.

## Trust And Architecture

- [Architecture Overview](architecture-overview.md) - public system model for the desktop app, local runtime, website trust layer, and AI providers.
- [Local-First Architecture](local-first-architecture.md) - high-level architecture for the desktop shell, local runtime, frontend workspace, and website trust layer.
- [Runtime Boundaries](runtime-boundaries.md) - what runs locally, what the website does, and what providers control.
- [Public Data Flows](data-flows.md) - sanitized flow summaries for prompts, model discovery, reasoning models, licensing, updates, and files.
- [Security and Trust Model](security-and-trust.md) - public trust boundary, prompt path, key handling, and customer responsibilities.
- [Security Section](../security/README.md) - private vulnerability reporting and public security posture.
- [Public Trust Boundaries](../security/trust-boundaries.md) - trust-zone reference for evaluators.

## Providers And Models

- [Provider Manager](provider-manager.md) - provider maintenance, model sync, saved discovery, and mode mapping.
- [Provider Orchestration](provider-orchestration.md) - provider differences, request shaping, mode mappings, and model policy at a public level.
- [Reasoning Models](reasoning-models.md) - reasoning-capable model behavior, unsupported settings, provider defaults, latency, and cost expectations.

## Product Boundaries

This repository documents public behavior and integration concepts. It does not include:

- Proprietary application source code
- Internal APIs that are not public product interfaces
- Secrets, keys, or environment files
- Deployment configuration or infrastructure automation
- Customer data
- Private repository history
- Internal audit findings or unresolved internal security gap lists
