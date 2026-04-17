# Quickstart

Use this guide to go from a fresh KeyRing AI install to a first successful provider response. It covers the public product flow only and does not include proprietary application source code.

## Prerequisites

You need:

- Windows 10 or later, 64-bit
- A KeyRing AI account and active license
- The KeyRing AI desktop installer from the official download page
- At least one AI provider account with API access
- A provider API key generated in that provider's official dashboard
- Provider billing, credits, or quota where the provider requires them

## Install And Activate

1. Sign in to the KeyRing AI website.
2. Copy your license key from the dashboard.
3. Download the Windows desktop installer from the official download page.
4. Install and launch KeyRing AI.
5. Paste the license key when prompted.
6. Wait for the local desktop runtime to finish first-launch initialization.

A successful activation means the desktop app can verify your license and enable the product features available to your plan.

## Connect One Provider

KeyRing AI uses a bring-your-own-key provider model.

1. Open API Settings.
2. Choose one provider to configure first.
3. Open that provider's official API dashboard.
4. Create or reveal a new API key.
5. Copy the key immediately if the provider only shows it once.
6. Paste the key into the matching provider card in KeyRing AI.
7. Save changes.
8. Select a model your provider account can access.
9. Enable the provider in the workspace controls.

Provider billing, model access, quotas, outages, and data handling remain controlled by the provider.

## Send A First Prompt

Start with one enabled provider and a small prompt:

```text
Say hello in one sentence and identify which provider/model is responding.
```

Expected result: the provider tab returns a response. If the tab errors, check the provider dashboard for API key validity, billing, quota, and selected model access.

## Compare Two Providers

After one provider works, add a second provider and use a comparison prompt:

```text
Compare three approaches to reduce cold start latency in desktop AI apps. Include tradeoffs and a recommended implementation order.
```

Expected result: each enabled provider responds in its own surface, giving you a side-by-side comparison of output quality, latency, and style.

## Try Provider Manager

Provider Manager is useful when providers add or rename models.

1. Open Provider Manager.
2. Select a provider.
3. Run Model Discovery or Sync.
4. Review the discovered model list.
5. Save the discovery result.
6. Map product modes such as Default or Reasoning to models available in the saved inventory.

Saved discovery results are what make newly found models durable in KeyRing AI. Provider account access still determines whether a model can actually be used.

## First-Run Troubleshooting

- **License rejected:** confirm the license key was copied exactly and belongs to the account you are using.
- **Provider auth error:** generate a new provider API key and save it again.
- **Model unavailable:** select a model your provider account can access.
- **Billing or quota error:** resolve the provider-side billing or credit issue.
- **No response in a tab:** confirm the provider is enabled in the active workspace.
- **Advanced setting rejected:** remove unsupported settings and retry with provider defaults.

## Next Steps

- Read [Getting Started](getting-started.md) for the full onboarding path.
- Read [Provider API Keys](provider-api-keys.md) for key setup and safety guidance.
- Read [Provider Manager](provider-manager.md) for model discovery and mode mapping.
- Read [Security and Trust Model](security-and-trust.md) to understand the local-first trust boundary.
- Read [Workflow Examples](../examples/README.md) for concrete public usage examples.
