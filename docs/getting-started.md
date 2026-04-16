# Getting Started With KeyRing AI

KeyRing AI is a Windows desktop application for working with multiple AI providers from one local-first interface. It lets you compare answers side by side, run multi-AI discussions, attach files for context, and track usage without switching between provider websites.

## Platform Availability

KeyRing AI is currently available for Windows 10 and later, 64-bit. macOS and Linux builds are planned separately.

## What You Can Do

- Query multiple AI providers from one workspace, subject to your plan and provider access.
- Compare model output in Chatroom view or individual provider tabs.
- Run Roundtable sessions where multiple AI systems discuss the same topic.
- Build and run custom AI agents where supported by your product tier.
- Attach files and control which providers receive that context.
- Keep provider API key handling local to your desktop environment.

## Onboarding Path

The basic setup path has three parts:

1. Get your KeyRing AI license.
2. Install and activate the desktop app.
3. Connect provider accounts and send your first prompt.

## Get Your License

1. Create a KeyRing AI account through the official website.
2. Verify your email if required.
3. Choose the appropriate plan or beta path.
4. Copy your license key from the dashboard.

Keep your license key private. It is used to activate the desktop app and determine the features available to your installation.

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

## Attachments Quickstart

The desktop app supports attaching files as context for provider requests.

Public behavior to understand:

- Attachments can be scoped globally or to specific providers.
- You can control how much of a file is sent as context.
- Lower-context modes can send metadata or filenames instead of full file contents.
- Provider-scoped attachments help compare providers with different evidence.

Do not place private customer data, secrets, or proprietary source code into public examples.

## Troubleshooting

Common first-run issues:

- **Provider auth error:** regenerate the provider API key and save it again.
- **Provider does not respond:** confirm billing, quota, and selected model access in the provider dashboard.
- **No output in a tab:** confirm the provider is enabled in the active workspace controls.
- **Plan restriction:** confirm the provider is included in your KeyRing AI license tier.
- **First launch feels slow:** this is expected while the local runtime initializes.
