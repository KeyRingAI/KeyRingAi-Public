# Local-First Architecture

KeyRing AI is a desktop application with a local runtime and a separate website trust layer. This document explains the public architecture at a high level.

## High-Level Model

KeyRing AI has four public-facing architectural concepts:

1. Desktop shell
2. Local backend runtime
3. Frontend workspace
4. Website account, license, download, and update layer

The product is not a cloud prompt relay. Normal provider requests are intended to run from the local desktop runtime to the selected provider.

## Desktop Shell

The native desktop shell is responsible for desktop application concerns such as:

- App launch
- Native window behavior
- Local runtime lifecycle
- Desktop update wiring
- Operating-system integration

This layer is intentionally separate from provider business logic.

## Local Backend Runtime

The local backend runtime handles the desktop application's local orchestration responsibilities, including:

- Provider request routing
- Provider settings
- Local persistence
- Runtime request shaping
- Workflow coordination
- Local key usage for provider calls

The public guarantee is the architectural boundary, not the proprietary implementation details.

## Frontend Workspace

The frontend workspace is the user-facing desktop interface. It exposes product workflows such as:

- Chatroom and provider tabs
- Multi-provider querying
- Attachments
- Roundtables
- Agent workflows where available
- API Settings
- Provider Manager
- History and metrics

## Website Layer

The website is separate from the normal prompt path. Its public roles include:

- Account access
- Pricing and plan information
- License distribution and validation
- Download access
- Update metadata
- Support and public documentation

The website layer is part of commercial trust and product delivery. It is not the routine relay for customer prompts and provider responses.

## Normal Prompt Flow

A simplified normal prompt flow looks like this:

```text
1) User enters a prompt in the desktop workspace
2) Local runtime prepares the request
3) Local runtime uses the selected provider configuration
4) Request is sent to the selected AI provider
5) Response returns to the desktop workspace
6) Local workflow surfaces display, compare, store, or export the result
```

## Why This Matters

This design is intended to make the system easier to reason about:

- The product can support multiple providers without becoming a universal prompt middleman.
- Customers keep provider account relationships directly with providers.
- Website trust flows are separated from normal AI request execution.
- The local runtime has a clear role in request orchestration and workflow state.

## Public Documentation Boundary

This document describes public architecture concepts. It does not disclose proprietary source code, internal service configuration, private deployment details, or security-sensitive implementation internals.
