# Security

This section describes KeyRing AI's public security posture at a high level. It is written for customers, developers, and evaluators who want to understand the product's trust boundaries without exposing proprietary implementation details.

The core KeyRing AI application source code is proprietary and is not included in this repository.

## Report Security Issues Privately

Please report suspected security issues privately.

Do not open public GitHub issues for suspected vulnerabilities, security bugs, credential exposure, abuse paths, privacy concerns, or suspected leaks of private materials.

Security contact: support@keyringlabs.com

Recommended subject line: `SECURITY: <short summary>`

If a dedicated security mailbox is created later, this file should be updated before announcing it publicly.

## What To Include In A Report

Include a clear description of the issue, safe reproduction steps, affected product area, potential impact, relevant screenshots or logs with secrets removed, app version if applicable, provider involved if relevant, and your preferred contact information for follow-up.

Do not include real provider API keys, license keys, customer data, private prompts, credentials, or private files in a report unless explicitly requested through a private channel.

## Public Security Model

KeyRing AI is designed around a local-first desktop model.

For normal provider usage, the public trust model is:

```text
User device -> KeyRing AI desktop workspace -> selected AI provider
```

The website participates in account, license, download, update, pricing, and support flows. It is not designed to be the routine relay for customer prompts and model responses.

## Security Principles

KeyRing AI's public security posture is organized around local-first operation, clear trust boundaries, bring-your-own-provider-key usage, scoped local runtime access, local secret handling, capability minimization, and separation between commercial trust flows and prompt execution.

Local-first does not mean providers never receive data. If a user sends a prompt, attachment, tool input, or generated context to a provider, that provider receives it under its own terms.

## What This Repository Does Not Publish

This public repository does not publish proprietary application source code, private business logic, exact security control internals, endpoint implementation details, secrets, keys, certificates, environment files, private infrastructure diagrams, deployment automation, customer data, private logs, exploit narratives, bypass recipes, internal audit findings, or unresolved security gap lists.

## Customer Responsibilities

Customers should keep the desktop app and operating system updated, protect provider API keys, rotate exposed credentials immediately, review provider terms and retention policies, avoid sending secrets or regulated data to unapproved providers, use separate provider keys where possible, review exports before sharing, and report suspected security issues privately.

## Related Documents

- [Reporting vulnerabilities](reporting-vulnerabilities.md)
- [Public trust boundaries](trust-boundaries.md)
- [Local runtime safety](local-runtime-safety.md)
- [Provider data responsibility](provider-data-responsibility.md)
- [Security and trust model](../docs/security-and-trust.md)
- [Local data and privacy](../docs/local-data-and-privacy.md)
