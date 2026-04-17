# Getting Started With KeyRing AI

KeyRing AI is a Windows desktop application for working with multiple AI providers from one local-first interface. It lets you compare answers side by side, run multi-AI discussions, attach files for context, and track usage without switching between provider websites.

## Platform Availability

KeyRing AI is currently available for Windows 10 and later, 64-bit. macOS and Linux builds are not part of the current public desktop release.

## Core Concepts

Before installing, understand the product model:

- **Desktop-first:** normal AI work happens in the desktop app.
- **Bring your own provider keys:** you connect your own provider accounts.
- **Direct provider path:** normal prompts go from your machine to the provider you select.
- **Website trust layer:** the website handles account, license, downloads, updates, support, pricing, and docs.
- **Provider differences matter:** each provider controls its own models, billing, quotas, API rules, and data terms.

## What You Can Do

- Query multiple AI providers from one workspace, subject to your plan and provider access.
- Compare model output in Chatroom view and provider-specific response surfaces.
- Run Roundtable sessions where multiple AI systems discuss the same topic.
- Build and run custom AI agents where supported by your product tier.
- Attach files and control which providers receive that context.
- Discover provider models and map product modes to available models.
- Keep provider API key handling local to your desktop environment.

## First Hour Checklist

A practical first-hour setup looks like this:

1. Create or sign in to your KeyRing AI account.
2. Copy your license key from the dashboard.
3. Install the Windows desktop app from the official download page.
4. Activate the app with your license key.
5. Configure one provider API key.
6. Send a short single-provider prompt.
7. Add a second provider.
8. Compare both providers on the same prompt.
9. Open Provider Manager and run Model Discovery for one provider.
10. Save the discovery result and verify the provider still works in the workspace.

## Get Your License

1. Create a KeyRing AI account through the official website.
2. Verify your email if required.
3. Choose the appropriate plan or beta path.
4. Copy your license key from the dashboard.

Keep your license key private. It activates the desktop app and determines the features available to your installation.

## Install And Activate

1. Download the Windows installer from the official download page.
2. Run the installer and launch KeyRing AI.
3. On first launch, allow the local runtime to initialize.
4. Paste your license key into the activation flow.
5. Save or validate the license when prompted.

The first launch can take longer than later launches because the local desktop runtime initializes behind the scenes.

## Connect Providers

KeyRing AI does not provide shared model access. You connect your own provider accounts.

1. Open API Settings.
2. Select the provider you want to configure.
3. Use the provider card link to open that provider's official dashboard.
4. Create or sign in to the provider account.
5. Add billing or credits if the provider requires them.
6. Generate a provider API key.
7. Paste the key into the matching KeyRing provider card.
8. Save changes.
9. Select a model available to your provider account.
10. Enable the provider in the workspace controls.

## Send Your First Prompt

Start with one provider enabled:

```text
Say hello and confirm you are responding from this provider.
```

Then enable two or more providers and compare results:

```text
Compare the pros and cons of three different product launch strategies. Give a concise recommendation at the end.
```

## Use Attachments Deliberately

The desktop app supports attaching files as context for provider requests.

Public behavior to understand:

- Attachments can be scoped globally or to specific providers.
- You can control how much of a file is sent as context.
- Lower-context modes can send metadata or filenames instead of full file contents.
- Provider-scoped attachments help compare providers with different evidence.

Do not send secrets, regulated data, customer data, or proprietary source code to a provider unless that provider and workflow are approved for that data.

## Use Model Discovery

Provider model catalogs change frequently. Use Provider Manager when:

- A provider releases a new model.
- A model disappears or is renamed.
- You need to map a product mode to a different model.
- A provider error suggests the selected model is not available.

Discovery results must be saved before they become durable in KeyRing AI.

## Troubleshooting

Common first-run issues:

- **Provider auth error:** regenerate the provider API key and save it again.
- **Provider does not respond:** confirm billing, quota, and selected model access in the provider dashboard.
- **No output in a tab:** confirm the provider is enabled in the active workspace controls.
- **Plan restriction:** confirm the provider is included in your KeyRing AI license tier.
- **First launch feels slow:** this is expected while the local runtime initializes.
- **Newly discovered model fails:** confirm your provider account actually has access and retry without unsupported advanced settings.

## Where To Go Next

- [Quickstart](quickstart.md)
- [Provider API Keys](provider-api-keys.md)
- [Provider Manager](provider-manager.md)
- [Reasoning Models](reasoning-models.md)
- [Security and Trust Model](security-and-trust.md)
