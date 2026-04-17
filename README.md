# KeyRing AI Developer Resources

This repository is the public documentation home for KeyRing AI. It gives customers, developers, and evaluators a clear view of how the product is intended to work without publishing the proprietary application source code.

KeyRing AI is a local-first Windows desktop application for working with multiple AI providers from one interface. The desktop app uses the user's own provider accounts and provider API keys. The KeyRing website handles account, license, download, update, support, pricing, and documentation flows; it is not the routine relay for customer prompts and model responses.

## What Is Included

- Public onboarding and quickstart documentation
- Local-first architecture and runtime-boundary explanations
- Security and trust-boundary documentation
- Bring-your-own-provider-key setup guidance
- Provider Manager and Model Discovery guidance
- Provider orchestration and reasoning-model behavior notes
- Public workflow examples that do not include proprietary source code
- Repository notices, proprietary boundaries, and changelog entries

## What Is Not Included

- The proprietary KeyRing AI application source code
- Private business logic or implementation details
- Deployment configuration or infrastructure automation
- Secrets, credentials, tokens, certificates, or environment files
- Customer data, private prompts, private logs, or operational data
- Internal tools, release scripts, or private infrastructure details
- Internal audit findings or unresolved internal security gap lists
- Any copy of the private application repository history

## Documentation Map

Start here if you are evaluating or onboarding:

- [Quickstart](docs/quickstart.md)
- [Getting Started](docs/getting-started.md)
- [Provider API Keys](docs/provider-api-keys.md)
- [Workflow Examples](examples/README.md)

Use these docs to understand the product model:

- [Architecture Overview](docs/architecture-overview.md)
- [Local-First Architecture](docs/local-first-architecture.md)
- [Runtime Boundaries](docs/runtime-boundaries.md)
- [Public Data Flows](docs/data-flows.md)
- [Security and Trust Model](docs/security-and-trust.md)
- [Public Trust Boundaries](security/trust-boundaries.md)

Use these docs when working with models and providers:

- [Provider Manager](docs/provider-manager.md)
- [Provider Orchestration](docs/provider-orchestration.md)
- [Reasoning Models](docs/reasoning-models.md)

Security reporting:

- [Security Section](security/README.md)

Full index:

- [Documentation Index](docs/index.md)

## Product Boundaries In One Minute

- KeyRing AI is desktop-first, not a hosted prompt relay.
- Normal prompt execution goes from the user's desktop environment to the selected AI provider.
- Users bring their own provider accounts and provider API keys.
- Provider availability, billing, rate limits, retention, and model access remain controlled by each provider.
- Website services are used for commercial trust and product delivery, not routine prompt proxying.
- This repository is public documentation only; the application remains proprietary.

## Links

- Website: https://keyringlabs.com
- Pricing: https://keyringlabs.com/pricing
- Support: support@keyringlabs.com
- Documentation: https://keyringlabs.com/docs

## Notice

See [NOTICE.md](NOTICE.md). The core KeyRing AI product remains proprietary and is not included in this repository.
