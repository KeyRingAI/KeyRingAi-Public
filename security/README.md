# Security

This section describes the public security posture for KeyRing AI at a high level. It is written for customers, developers, and evaluators who want to understand the product's trust boundaries without exposing proprietary implementation details.

The core application source code is proprietary and is not included in this repository.

## Report Security Issues Privately

Please report suspected security issues privately.

Do not open public GitHub issues for suspected vulnerabilities, security bugs, credential exposure, abuse paths, privacy concerns, or suspected leaks of private materials.

Security contact: support@keyringlabs.com

Subject line: `SECURITY: <short summary>`

If a dedicated security mailbox is created later, this file should be updated before announcing it publicly.

## What To Include In A Report

When reporting a security issue, include as much detail as you can safely share:

- A clear description of the issue
- Steps to reproduce, if safe to share
- The affected product area or public resource
- Potential impact
- Screenshots, logs, or proof-of-concept details with secrets removed
- Your preferred contact information for follow-up

Do not include real provider API keys, license keys, customer data, private prompts, or credentials in a report unless explicitly requested through a private channel.

## Public Security Overview

KeyRing AI is designed around a local-first desktop model.

For normal AI provider usage, the public trust model is:

```text
User device -> KeyRing AI local desktop runtime -> selected AI provider
```

KeyRing website services participate in account, license, download, update, and support flows. They are not designed to be the routine relay for customer prompts and model responses.

## Security Principles

KeyRing AI's public security posture is organized around these principles:

- **Local-first runtime:** normal provider work happens from the desktop environment, not through a hosted prompt relay.
- **Clear trust boundaries:** website commercial flows, desktop runtime flows, provider calls, and local user data are treated as separate concerns.
- **Bring your own provider keys:** users connect their own provider accounts and manage provider billing, limits, and terms directly with those providers.
- **Scoped local session access:** the desktop interface talks to the local runtime through a session boundary rather than an open network service model.
- **Local secret handling:** provider credentials are handled by the desktop environment and are not copied into a shared KeyRing cloud vault for routine prompt execution.
- **Capability minimization:** native actions, external opens, and local tool-like behaviors are treated as sensitive capabilities rather than generic free-form operations.
- **Commercial trust separation:** licensing and update checks are separate from normal prompt execution.

## High-Level Trust Boundaries

KeyRing AI separates security responsibilities into several public boundaries:

### Website To Desktop Commercial Trust

The website handles account, license, download, and update-related trust. The desktop validates entitlement state before enabling gated product behavior.

Public takeaway: commercial access is separate from normal prompt relay behavior.

### Desktop Shell To Local Runtime

The desktop shell owns launch and lifecycle responsibilities for the local runtime. The runtime is treated as a local component of the desktop app, not as a general internet service.

Public takeaway: local runtime startup is bounded and supervised by the desktop app.

### Desktop Interface To Local Runtime

The user interface communicates with the local runtime through local session controls. Browser-like state-changing requests are treated carefully, and the runtime is not intended to accept arbitrary remote callers.

Public takeaway: the local app boundary is deliberately narrower than a public web API.

### Local Runtime To AI Providers

Provider requests are sent using the user's own provider configuration and provider API credentials.

Public takeaway: KeyRing AI does not replace the user's direct relationship with AI providers.

### Local Secrets And User Data

Provider keys, license state, local history, files, and workflow state are desktop-side concerns. Customers remain responsible for deciding what data is appropriate to send to each selected AI provider.

Public takeaway: local-first does not mean providers never receive data. If a user sends a prompt or attachment to a provider, that provider receives it under its own terms.

### Native Capability Perimeter

Native operations such as opening external locations, interacting with local files, clipboard-like actions, and automation-style behaviors are handled as sensitive capabilities. Public examples in this repository must not include private source code or unsafe local automation recipes.

Public takeaway: capability boundaries are part of the product design, but this public repository intentionally does not disclose implementation-level enforcement details.

## Automation And Tool Safety Stance

AI-driven tools and automation require stricter review than ordinary chat because they can create side effects. Public documentation should describe the safety posture without publishing bypass-oriented details.

Public-safe principles:

- Risky local actions should be minimized, scoped, or disabled unless explicitly supported.
- User approval should be required for sensitive actions where appropriate.
- Filesystem access should be limited to intentional user-selected scope.
- Network access by automation should be treated as a sensitive capability.
- Secrets should not be exposed to automation contexts that do not need them.
- Future automation features should be reviewed against the actual implementation before being documented as production behavior.

## What This Repository Intentionally Does Not Publish

To avoid creating an attacker roadmap, this public repository does not publish:

- Internal source code
- Exact token, session, or entitlement internals
- Internal configuration names or deployment details
- Private endpoint implementation details
- Internal audit findings or unresolved internal gap lists
- Exploit narratives or bypass recipes
- Private infrastructure diagrams
- Secrets, customer data, logs, keys, certificates, or environment files

## Customer Responsibilities

Customers should:

- Keep the desktop app and operating system updated.
- Protect provider API keys and rotate any exposed key immediately.
- Review each provider's terms, retention policy, and data handling rules.
- Avoid sending secrets or regulated data to providers unless that workflow is approved for the data.
- Use separate provider keys for different environments where possible.
- Report suspected security issues privately.

## Repository Scope

This public repository contains documentation and public developer resources only. The proprietary KeyRing AI application source code is not included here.

If you discover secrets, private configuration, customer data, proprietary source code, or internal infrastructure details in this public repository, report it privately immediately.

## Related Documents

- [Public trust boundaries](trust-boundaries.md)
- [Security and trust model](../docs/security-and-trust.md)
- [Local-first architecture](../docs/local-first-architecture.md)
