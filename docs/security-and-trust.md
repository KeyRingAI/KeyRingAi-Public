# Security And Trust Model

This document summarizes the public KeyRing AI security and privacy model. It is intentionally high-level and does not expose proprietary implementation details.

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
- Licensing and update checks are separate website trust flows.

## Security Layers

### Direct Provider Path

Normal prompt execution goes from your machine through the local runtime to the selected AI provider. This narrows the trust boundary compared with cloud relay tools that proxy every prompt through their own service.

### Local Key Handling

Provider credentials are entered into the desktop app and used for direct provider calls. KeyRing AI does not require customers to give KeyRing a central copy of all provider keys for routine prompt execution.

### Loopback Runtime

The desktop backend is designed as a local runtime, not a public internet service. The user interface talks to the local runtime rather than exposing a general network backend for normal app use.

### Separate Commercial Trust Flows

The website participates in account, license, download, and update flows. Those flows are separate from routine provider prompt execution.

## What KeyRing AI Does Not Claim

This public documentation should not be read as a guarantee that third-party providers do not receive data. If you send a prompt to a provider, that provider receives the request according to its API terms and privacy policy.

KeyRing AI also cannot control:

- Provider retention or training policies
- Provider rate limits or outage behavior
- Provider billing decisions
- Provider model access decisions
- Local device compromise outside the app boundary

## Customer Responsibilities

Customers should:

- Review each provider's terms before sending sensitive data.
- Use provider accounts and keys appropriate for their risk model.
- Rotate exposed keys immediately.
- Avoid putting secrets into prompts or attachments unless the provider and workflow are approved for that data.
- Keep the desktop app and operating system updated.

## Public Repository Boundary

This GitHub repository contains public documentation only. It does not contain proprietary source code, private deployment configuration, secrets, certificates, customer data, or private infrastructure details.

## Security Reporting

Report suspected vulnerabilities privately. Do not open public GitHub issues for suspected security problems.

See [security reporting](../security/README.md).
