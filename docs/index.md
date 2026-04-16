# KeyRing AI Public Documentation

This folder contains public-facing KeyRing AI documentation intended to help customers, developers, and evaluators understand the product without exposing proprietary application source code.

The documents here are derived from public website documentation and marketing pages, then adapted for a GitHub documentation format. They intentionally avoid private implementation details, internal deployment configuration, source code, secrets, and customer data.

## Start Here

- [Quickstart](quickstart.md) - shortest path from evaluation to first working prompt.
- [Getting Started](getting-started.md) - broader onboarding flow for license, install, provider keys, and first use.
- [Provider API Keys](provider-api-keys.md) - bring-your-own-key setup guidance.

## Trust And Architecture

- [Security and Trust Model](security-and-trust.md) - public trust boundary, prompt path, key handling, and reporting guidance.
- [Local-First Architecture](local-first-architecture.md) - high-level architecture for the desktop shell, local runtime, frontend workspace, and website trust layer.

## Product Operations

- [Provider Manager](provider-manager.md) - public workflow guide for provider registry maintenance and model discovery.
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
