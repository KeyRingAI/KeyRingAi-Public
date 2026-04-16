# Security And Trust Model

This document summarizes the public KeyRing AI security and privacy model. It is intentionally high-level and does not expose proprietary implementation details.

For the public security section and private reporting instructions, see [security](../security/README.md).

## Core Trust Boundary

KeyRing AI is designed around a local-first desktop runtime.

For normal prompt execution, the working path is:

```text
You -> KeyRing AI desktop runtime on your machine -> selected AI provider
```

The KeyRing website is not the routine chat relay for normal provider usage.

## What This Means

- Normal prompt traffic is not relayed through KeyRing servers.
- Provider requests are dispatched from the desktop environment to the selected provider.
- Provider API keys are handled by the desktop app rather than a shared cloud provider vault.
- Conversation history and workflow state are local desktop concerns, not a hosted chat service model.
- Licensing, downloads, support, and updates are separate website trust flows.

## Public Security Layers

### Direct Provider Path

Normal prompt execution goes from the user's machine through the local runtime to the selected AI provider. This narrows the trust boundary compared with cloud relay tools that proxy every prompt through their own service.

### Local Key Handling

Provider credentials are entered into the desktop app and used for direct provider calls. KeyRing AI does not require customers to give KeyRing a central copy of all provider keys for routine prompt execution.

### Scoped Local Runtime

The desktop runtime is designed as a local application component, not a public internet service. The interface talks to the local runtime through local session controls rather than exposing a broad remote API surface.

### Separate Commercial Trust Flows

The website participates in account, license, download, update, and support flows. Those flows are separate from routine provider prompt execution.

### Capability Minimization

Native desktop actions, local file interactions, external opens, and automation-style behaviors are treated as sensitive capabilities. Public documentation describes the design posture without publishing low-level enforcement details.

## Provider Trust Still Matters

Local-first does not mean third-party providers never receive data.

If a user sends a prompt, file, or generated context to a selected provider, that provider receives the request under its own terms, data handling practices, retention policy, rate limits, and billing model.

## What KeyRing AI Does Not Claim

This public documentation should not be read as a guarantee that:

- AI providers never receive data.
- Provider retention policies are controlled by KeyRing AI.
- Provider billing, quotas, outages, or model access decisions are controlled by KeyRing AI.
- Local device compromise is solved by the application boundary alone.
- Public documentation contains every internal security control or review result.

## Customer Responsibilities

Customers should:

- Review each provider's terms before sending sensitive data.
- Use provider accounts and keys appropriate for their risk model.
- Rotate exposed keys immediately.
- Avoid putting secrets into prompts or attachments unless the provider and workflow are approved for that data.
- Keep the desktop app and operating system updated.
- Report suspected vulnerabilities privately rather than through public GitHub issues.

## Public Repository Boundary

This GitHub repository contains public documentation only. It does not contain proprietary source code, private deployment configuration, secrets, certificates, customer data, internal audit detail, or private infrastructure information.

## Related Documents

- [Security section](../security/README.md)
- [Public trust boundaries](../security/trust-boundaries.md)
- [Local-first architecture](local-first-architecture.md)
