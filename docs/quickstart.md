# Quickstart

This quickstart gives a public, high-level path for evaluating KeyRing AI and sending a first prompt. It does not include proprietary application source code or private implementation details.

## Prerequisites

- Windows 10 or later, 64-bit
- A KeyRing AI account and active license
- The KeyRing AI desktop installer from the official download page
- At least one AI provider account that supports API access
- A provider API key created in that provider's official dashboard
- Provider-side billing or credits where required by that provider

## Setup

1. Create or access your KeyRing AI account.
2. Obtain your license key from the KeyRing dashboard.
3. Download and install the Windows desktop app from the official download page.
4. Launch KeyRing AI.
5. Paste your license key when prompted and activate the app.
6. Open API Settings.
7. Add at least one provider API key.
8. Choose a model that your provider account can access.
9. Enable the provider in the workspace controls.

## Authentication And Provider API Keys

KeyRing AI uses a bring-your-own-key model for AI provider access.

That means:

- You create provider accounts directly with the AI providers you want to use.
- You generate provider API keys in those providers' official dashboards.
- You paste each key into the matching provider card in KeyRing AI.
- Normal prompt execution uses your provider credentials from the desktop app.
- Provider billing, quotas, model access, and terms are controlled by the provider.

Do not commit real API keys, tokens, credentials, certificates, or `.env` files to this repository.

## First Example Prompt

After license activation and provider setup, enable one provider and send a simple prompt:

```text
Say hello and confirm which provider/model is responding.
```

Then try a comparison prompt with more than one provider enabled:

```text
Compare three approaches to reduce cold start latency in desktop AI apps. Include tradeoffs and a recommended implementation order.
```

## Next Steps

- Read [Getting Started](getting-started.md) for the full onboarding path.
- Read [Provider API Keys](provider-api-keys.md) for account, billing, and key setup guidance.
- Read [Security and Trust Model](security-and-trust.md) to understand the local-first trust boundary.
- Read [Local-First Architecture](local-first-architecture.md) to understand the desktop runtime model.
