# Provider Orchestration

KeyRing AI is built to work across multiple AI providers without forcing every provider into the same shape. This document explains the public provider orchestration model.

## Why Orchestration Exists

AI providers differ across:

- Authentication requirements
- Model names and release cadence
- Context windows and output limits
- Streaming formats
- Tool-calling support
- Reasoning controls
- Image, vision, video, and search capabilities
- Pricing and usage fields
- Error messages and rate limits

A reliable multi-provider desktop app needs a layer that understands those differences.

## What KeyRing Normalizes

Publicly, KeyRing AI normalizes the experience around:

- Provider activation and key status
- Provider model inventory
- Model Discovery and saved model catalogs
- Provider mode mappings
- Request shaping per provider and model
- Response display across provider tabs
- Usage and cost awareness where provider data allows it
- Local history, exports, and workflow state

This does not mean every provider becomes identical. It means the product tries to present a coherent workflow while respecting provider-specific rules.

## Model Discovery

Model Discovery helps users sync a provider's available models into KeyRing.

The expected public behavior is:

1. Discovery asks the provider for available models.
2. The user reviews the discovered list.
3. The user saves the result.
4. Saved models become part of KeyRing's provider inventory.
5. Mode mappings and provider policies determine how those models are used.

Model Discovery is most useful when providers release new models or change model names. Provider account access still matters: a model may be visible but unavailable to the user's provider account or plan.

## Model Policy Layer

The model policy layer is the public concept that keeps provider requests from being one-size-fits-all.

It decides which controls are appropriate for the selected provider and model. Examples of controls that can vary include:

- Temperature
- Top-p
- Maximum output length
- Reasoning effort or thinking mode
- Tool definitions
- Streaming behavior
- Mode-specific options

If a model does not support a control, the correct product behavior is usually to omit that control or fall back to the provider's default rather than forcing an invalid request.

## Provider Modes

Provider modes are a way to connect product workflows to provider models. Common modes include:

| Mode | Public Meaning |
| --- | --- |
| Default | General chat or general-purpose completion. |
| Reasoning | Models intended for deeper problem solving where supported. |
| Vision | Models that can accept image input where supported. |
| Image | Image generation or image editing workflows where supported. |
| Video | Video generation or video-related workflows where supported. |
| Deep research | Search or research-oriented models where supported. |

Mode availability depends on the provider and the user's account.

## Reasoning Controls Are Not Universal

Reasoning-capable models are a good example of why provider-aware orchestration matters.

One provider may accept an explicit effort setting. Another may use a different field. Another may expose reasoning behavior through the model itself and reject extra controls. A reasoning model may also reject standard sampling settings that ordinary chat models accept.

KeyRing's public design goal is to make the model usable as soon as it is discovered and saved, while applying provider and model policy so unsupported settings do not cause avoidable failures.

## Customer Evaluation Questions

When evaluating provider support, ask:

- Does my provider account have access to this model?
- Did I save the model after discovery?
- Is the model mapped to the provider mode I want to use?
- Does the model accept the settings I enabled?
- Is the error coming from KeyRing, the provider account, or the provider API?

## Documentation Boundary

This document describes public product behavior. It does not disclose proprietary routing code, private provider registry implementation, internal endpoint design, test fixtures, deployment details, or private provider-maintenance procedures.
