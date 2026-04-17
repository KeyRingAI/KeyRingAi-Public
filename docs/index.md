# KeyRing AI Public Documentation

This folder contains public-facing KeyRing AI documentation for customers, developers, and evaluators. It explains product behavior, onboarding, provider setup, architecture, workflows, and trust boundaries without exposing proprietary application source code.

## Start Here

- [Quickstart](quickstart.md) - install, activate, connect one provider, and send a first prompt.
- [Getting Started](getting-started.md) - original onboarding path for license, install, provider keys, first use, attachments, and Model Discovery.
- [Getting Started With The Desktop App](getting-started-desktop.md) - practical first-session guide grounded in the desktop workspace.
- [Desktop Workspace](desktop-workspace.md) - layout, navigation, status surfaces, and local-first product model.
- [Screenshot Gallery](screenshot-gallery.md) - public product screenshots for the main workspace and feature surfaces.
- [Workflow Examples](../examples/README.md) - concrete public-safe workflows and checklists.

## Core Workflows

- [Prompt Workflows](prompt-workflows.md) - prompt editor, system context, request options, modes, and prompt safety.
- [Chatroom And Provider Tabs](chatroom-and-provider-tabs.md) - when to use side-by-side provider tabs versus a unified transcript.
- [Attachments](attachments.md) - scoping, ingestion modes, and data handling guidance.
- [Prompt Presets](prompt-presets.md) - reusable prompts, tags, backup, import, and review practices.
- [History And Exports](history-and-exports.md) - local records, search, load, export, and deletion expectations.
- [Metrics And Costs](metrics-and-costs.md) - usage intelligence, estimated cost, latency, and export guidance.
- [Notifications And Status](notifications-and-status.md) - provider status, update state, long-running jobs, and issue reporting.
- [Settings](settings.md) - desktop notifications, app sizing, theme controls, and dangerous tool consent visibility.

## Providers And Models

- [Provider API Keys](provider-api-keys.md) - bring-your-own-key setup, provider readiness, and key hygiene.
- [Provider Setup](provider-setup.md) - practical provider onboarding and validation path.
- [Provider Manager](provider-manager.md) - provider maintenance, model sync, saved discovery, and mode mapping.
- [Model Discovery](model-discovery.md) - newly released models, saved discovery, and account-access caveats.
- [Model Configuration](model-configuration.md) - request shaping, profiles, unsupported settings, and provider defaults.
- [Provider Orchestration](provider-orchestration.md) - provider differences, request shaping, mode mappings, and model policy at a public level.
- [Reasoning Models](reasoning-models.md) - reasoning-capable model behavior, unsupported settings, provider defaults, latency, and cost expectations.
- [Troubleshooting Provider Errors](troubleshooting-provider-errors.md) - clean triage path for provider failures.

## Advanced Workflows

- [Roundtable](roundtable.md) - structured multi-provider discussion and evaluation.
- [Agents](agents.md) - local agent setup, templates, tools, memory, and safe review.
- [Tools And Consent](tools-and-consent.md) - public tool capability and dangerous-action consent model.
- [Media Generation](media-generation.md) - image and video workflow expectations.
- [Text To Speech](text-to-speech.md) - voice playback, provider setup, and sensitive content guidance.

## Trust, Privacy, And Architecture

- [Architecture Overview](architecture-overview.md) - public system model for the desktop app, local runtime, website trust layer, and AI providers.
- [Local-First Architecture](local-first-architecture.md) - high-level architecture for the desktop shell, local runtime, frontend workspace, and website trust layer.
- [Runtime Boundaries](runtime-boundaries.md) - what runs locally, what the website does, and what providers control.
- [Public Data Flows](data-flows.md) - sanitized flow summaries for prompts, model discovery, reasoning models, licensing, updates, and files.
- [Security and Trust Model](security-and-trust.md) - public trust boundary, prompt path, key handling, and customer responsibilities.
- [Local Data And Privacy](local-data-and-privacy.md) - local records, provider responsibility, website boundary, and export review.
- [License Activation And Updates](license-activation-and-updates.md) - commercial trust flow, tiers, update behavior, and troubleshooting.
- [Security Section](../security/README.md) - private vulnerability reporting and public security posture.
- [Public Trust Boundaries](../security/trust-boundaries.md) - trust-zone reference for evaluators.

## Product Boundaries

This repository documents public behavior and integration concepts. It does not include proprietary application source code, internal APIs that are not public product interfaces, secrets, keys, environment files, deployment configuration, infrastructure automation, customer data, private repository history, internal audit findings, or unresolved internal security gap lists.
