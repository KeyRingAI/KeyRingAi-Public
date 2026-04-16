# Architecture Overview

KeyRing AI is designed as a local-first desktop AI workspace with a separate website layer for commercial trust, downloads, updates, and support.

The important public idea is simple: normal AI work is performed from the user's machine to the selected provider. The KeyRing website is not the routine relay for customer prompts and model responses.

## Design Principles

KeyRing AI's architecture is built around a few customer-visible principles:

- Keep prompt execution local to the desktop runtime wherever possible.
- Let customers use their own provider accounts and provider API keys.
- Separate commercial trust flows from AI request execution.
- Support multiple providers without pretending their APIs are identical.
- Shape provider requests according to the selected provider and model.
- Keep native desktop capabilities scoped and separate from plain text chat.

## System Zones

| Zone | Public Role |
| --- | --- |
| Desktop shell | Launches the desktop application, manages native app behavior, and supervises the local runtime. |
| Local runtime | Handles provider orchestration, request shaping, local workflow state, and direct provider communication. |
| Desktop workspace | Presents the user interface for chat, multi-provider comparison, agents, files, history, metrics, and provider settings. |
| Website layer | Handles account, license, download, update, support, pricing, and public documentation flows. |
| AI providers | Execute model requests under the user's provider account, terms, rate limits, billing rules, and data policies. |

## What Runs Locally

The desktop app owns the normal AI workflow experience. That includes:

- Provider selection
- Model selection
- Provider API key usage
- Prompt preparation
- Request shaping
- Streaming or response display
- Conversation and workflow state
- Local file and export workflows

This local-first model is intended to make the prompt path easier to evaluate: the user chooses a provider, KeyRing prepares the request locally, and the selected provider processes it.

## What The Website Does

The website is part of product delivery and commercial trust. It supports:

- Account and plan workflows
- License access and validation
- Product downloads
- Update metadata
- Support and public documentation
- Administrative product operations where applicable

The website layer is separate from routine prompt execution. License and update checks should not be confused with prompt proxying.

## Provider-Aware Orchestration

AI providers differ in important ways. A setting that works for one provider may be unsupported, renamed, constrained, or ignored by another provider or model.

KeyRing AI is designed around provider-aware orchestration rather than one universal request shape. Publicly, that means the product needs to understand:

- Which provider is active
- Which model is selected
- Which provider mode is being used
- Which parameters are safe for that provider and model
- Which response fields can be normalized for display, history, metrics, and cost awareness

This is especially important for reasoning-capable models, image models, vision models, video models, and providers with rapidly changing model catalogs.

## What Customers Can Verify

Customers and evaluators can use this public repository to understand the intended trust and architecture model:

- The product is desktop-first, not a hosted chat relay.
- Provider accounts remain customer-owned.
- Website trust flows are separate from normal prompt execution.
- Provider differences are handled by a provider-aware orchestration layer.
- Public docs avoid exposing private implementation internals.

## Documentation Boundary

This document describes public architecture concepts. It does not disclose proprietary source code, private service configuration, internal route design, release automation, exact security controls, customer data, secrets, or private infrastructure details.
