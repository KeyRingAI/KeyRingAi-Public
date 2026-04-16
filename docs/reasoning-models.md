# Reasoning Models

Reasoning models are provider models intended for more deliberate problem solving, planning, analysis, or multi-step tasks. They can be useful for code review, technical diagnosis, math, research synthesis, and complex decision support.

This document explains KeyRing AI's public reasoning-model posture without exposing proprietary implementation details.

## What Makes Reasoning Models Different

Compared with ordinary chat models, reasoning-capable models may differ in several ways:

- They can take longer to answer.
- They may use additional hidden or summarized computation.
- They may have different token accounting.
- They may reject settings that ordinary chat models accept.
- They may expose provider-specific effort or thinking controls.
- They may cost more for complex prompts.

Customers should evaluate reasoning models under the provider's own documentation, terms, pricing, and data handling rules.

## How KeyRing Handles Reasoning Models

The public KeyRing design goal is to make reasoning models usable through the same provider workflow while respecting provider-specific rules.

At a high level, KeyRing should:

1. Discover models from the provider where discovery is available.
2. Save discovered models into the local provider inventory when the user confirms them.
3. Allow mode mapping so a reasoning workflow can point at an appropriate model.
4. Shape the request according to the selected provider and model.
5. Omit unsupported settings where the provider or model does not accept them.
6. Surface provider errors clearly enough for the user to distinguish account, model, quota, and parameter issues.

## Unsupported Settings And Provider Defaults

Reasoning models do not all accept the same configuration.

For example, some reasoning models should not receive temperature or other sampling controls. In those cases, the safer behavior is to omit the unsupported control and let the provider use its default behavior.

This is a normal part of multi-provider orchestration. It is not a sign that every model needs a separate public UI.

## Reasoning Effort

Some providers expose a reasoning effort, thinking budget, or similar control. Other providers do not. Even when providers expose a similar concept, accepted values and effects may differ.

KeyRing's public behavior should be understood as provider-aware rather than universal:

- If the selected model supports an effort control, KeyRing can include the appropriate control.
- If the selected model does not support it, KeyRing should avoid forcing that control.
- If the provider changes its API, model discovery and provider policy may need to adapt.

## What KeyRing Does Not Claim

This public documentation does not claim that:

- Every provider exposes reasoning in the same way.
- Every reasoning model exposes visible chain-of-thought content.
- KeyRing can override provider-side model access, billing, or rate limits.
- A discovered model is guaranteed to be usable by every provider account.
- Public docs include every internal provider policy or implementation detail.

## Best Practices

For reliable reasoning-model use:

- Confirm your provider account has access to the selected model.
- Save discovered models before mapping or using them.
- Map the reasoning mode to a model intended for reasoning tasks.
- Start with provider defaults when a model rejects advanced controls.
- Expect longer latency for deeper reasoning tasks.
- Review provider pricing before using high-effort reasoning on large prompts.

## Related Documents

- [Provider Orchestration](provider-orchestration.md)
- [Provider Manager](provider-manager.md)
- [Public Data Flows](data-flows.md)
- [Runtime Boundaries](runtime-boundaries.md)
