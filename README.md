# KeyRing AI Developer Resources

This repository is the public documentation home for KeyRing AI. It gives customers, developers, and evaluators a clear view of how the product is intended to work without publishing the proprietary application source code.

KeyRing AI is a local-first Windows desktop workspace for working with multiple AI providers from one interface. The desktop app uses the user's own provider accounts and provider API keys. The KeyRing AI website handles account, license, download, update, support, pricing, and documentation flows; it is not the routine relay for customer prompts and model responses.

## What Is Included

- Public onboarding and quickstart documentation
- Desktop workspace and workflow guides
- Provider setup, Provider Manager, and Model Discovery guidance
- Model configuration and request-shaping explanations
- Chatroom, Roundtable, Agent Builder, attachments, prompts, history, metrics, media, and text-to-speech documentation
- Local-first architecture and runtime-boundary explanations
- Security, privacy, and trust-boundary documentation
- Public workflow examples and checklists
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

## Start Here

- [Documentation Index](docs/index.md)
- [Quickstart](docs/quickstart.md)
- [Getting Started With The Desktop App](docs/getting-started-desktop.md)
- [Desktop Workspace](docs/desktop-workspace.md)
- [Examples](examples/README.md)
- [Security](security/README.md)

## Product Boundaries In One Minute

KeyRing AI is desktop-first, not a hosted prompt relay. Normal prompt execution goes from the user's desktop environment to the selected AI provider. Users bring their own provider accounts and provider API keys. Provider availability, billing, rate limits, retention, and model access remain controlled by each provider. Website services are used for commercial trust and product delivery, not routine prompt proxying. This repository is public documentation only; the application remains proprietary.

## High-Value Docs

- [Provider Setup](docs/provider-setup.md)
- [Model Discovery](docs/model-discovery.md)
- [Model Configuration](docs/model-configuration.md)
- [Roundtable](docs/roundtable.md)
- [Agents](docs/agents.md)
- [Tools And Consent](docs/tools-and-consent.md)
- [Local Data And Privacy](docs/local-data-and-privacy.md)
- [Troubleshooting Provider Errors](docs/troubleshooting-provider-errors.md)

## Links

- Website: https://keyringlabs.com
- Pricing: https://keyringlabs.com/pricing
- Support: support@keyringlabs.com
- Documentation: https://keyringlabs.com/docs

## Notice

See [NOTICE.md](NOTICE.md). The core KeyRing AI product remains proprietary and is not included in this repository.
