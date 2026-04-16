# KeyRing AI Public Documentation

This folder contains public-facing KeyRing AI documentation intended to help customers, developers, and evaluators understand the product without exposing proprietary application source code.

The documents here are derived from public website documentation and public-safe internal documentation themes, then adapted for a GitHub documentation format. They intentionally avoid private implementation details, internal deployment configuration, source code, secrets, and customer data.

## Start Here

- [Quickstart](quickstart.md) - shortest path from evaluation to first working prompt.
- [Getting Started](getting-started.md) - broader onboarding flow for license, install, provider keys, and first use.
- [Provider API Keys](provider-api-keys.md) - bring-your-own-key setup guidance.

## Trust And Architecture

- [Architecture Overview](architecture-overview.md) - public system model for the desktop app, local runtime, website trust layer, and AI providers.
- [Local-First Architecture](local-first-architecture.md) - high-level architecture for the desktop shell, local runtime, frontend workspace, and website trust layer.
- [Runtime Boundaries](runtime-boundaries.md) - customer-facing explanation of what runs locally, what the website does, and what providers control.
- [Public Data Flows](data-flows.md) - sanitized flow summaries for prompts, model discovery, reasoning models, licensing, updates, and files.
- [Security and Trust Model](security-and-trust.md) - public trust boundary, prompt path, key handling, and reporting guidance.
- [Security Section](../security/README.md) - private reporting instructions and public security posture.
- [Public Trust Boundaries](../security/trust-boundaries.md) - high-level trust-zone reference for evaluators.

## Providers And Models

- [Provider Manager](provider-manager.md) - public workflow guide for provider registry maintenance and model discovery.
- [Provider Orchestration](provider-orchestration.md) - how KeyRing handles provider differences, request shaping, mode mappings, and model policy at a public level.
- [Reasoning Models](reasoning-models.md) - customer-facing guide to reasoning-capable models, unsupported settings, provider defaults, and latency/cost expectations.

## Product Operations

- [Examples](../examples/README.md) - reserved for public examples only.
- [Security Reporting](../security/README.md) - private vulnerability reporting guidance.

## Public Documentation Boundary

This repository documents public behavior and integration concepts. It does not include:

- Proprietary application source code
- Internal APIs that are not public product interfaces
- Secrets, keys, or environment files
- Deployment configuration or infrastructure automation
- Customer data
- Private repository history
- Internal audit findings or unresolved internal security gap lists
