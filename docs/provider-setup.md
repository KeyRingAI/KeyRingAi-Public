# Provider Setup

KeyRing AI is a bring-your-own-key desktop workspace. The user connects provider accounts they already control, then chooses which providers and models to use for each workflow. This design keeps provider billing, access control, and model terms with the provider while giving the user a single local interface for orchestration and comparison.

![API Settings](../assets/screenshots/api-settings.png)

_Public screenshot: API Settings with provider cards, masked API keys, license state, selected models, and update controls._

## Supported Provider Categories

KeyRing AI is designed around major AI providers used for chat, reasoning, research, vision, image, video, and related workflows. Publicly documented provider slots include OpenAI, Anthropic, Google Gemini, Mistral, Groq, xAI, Cohere, DeepSeek, Together, and Perplexity. ElevenLabs can be configured for voice playback workflows.

Exact model availability changes frequently and is controlled by each provider. A provider key may be valid while a specific model remains unavailable because of account tier, region, preview status, billing state, rate limits, or provider-side rollout timing.

## Basic Setup Flow

Open API Settings from the desktop workspace. Select the provider you want to configure. Paste the provider API key into the key field, review any provider-specific options shown by the app, and save the change. The provider card should move from missing to configured or active once KeyRing AI recognizes the key.

After saving the key, open Provider Manager to review the provider's model list, model modes, routing labels, and display settings. If the provider supports discovery, use Model Discovery to refresh the local model inventory from the provider's public model-listing API.

Finally, send a short non-sensitive test prompt to confirm that the provider can complete an actual request. A configured key is necessary, but a successful request is the real validation that billing, access, model name, request shape, and provider account state are all aligned.

## Provider Access Is Not The Same As Model Access

Provider setup has several layers. The API key must be syntactically valid. The provider account must be active and allowed to use API services. Billing or credits may need to be enabled in the provider dashboard. The selected model must be available to the account. The selected model must support the requested mode, such as chat, reasoning, image, vision, video, or research. The request settings must be compatible with that model.

This layered model is why KeyRing AI separates API Settings, Provider Manager, Model Discovery, and Model Configuration. Each screen addresses a different part of provider readiness.

## Key Hygiene

Provider keys should be treated as sensitive credentials. Use dedicated API keys for KeyRing AI where the provider supports them. Prefer scoped keys, spending limits, usage alerts, and provider-side monitoring. Revoke keys immediately if they are exposed.

Do not paste provider keys into prompts, saved prompt presets, attachments, shared screenshots, public issue reports, or exported examples. If your organization uses shared machines, review local access policies before storing any provider credential.

## Tier And Feature Expectations

Some KeyRing AI features depend on the KeyRing AI license tier. Some provider features depend on the provider account tier. Those are separate controls. For example, a KeyRing AI tier may enable a workflow surface, while a provider account may still deny a specific model or tool because the provider has not enabled it for that account.

When troubleshooting, separate KeyRing AI readiness from provider readiness. If the desktop app accepts the provider key but the provider returns access, quota, or billing errors, the fix usually happens in the provider dashboard.

## Recommended Validation Path

Start with one provider and one well-known chat model. Send a short prompt without tools, attachments, or advanced settings. If that works, enable streaming or Chatroom routing. If that works, run Model Discovery. If that works, test a newly discovered model with conservative defaults. If that works, add attachments, tools, reasoning settings, media modes, or advanced model configuration one at a time.

This sequence keeps each test small enough to identify the layer that failed.

## Public Boundary

This document describes public setup behavior. It does not include provider secrets, internal source code, private validation logic, proprietary routing implementation, or deployment details.
