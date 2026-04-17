# Model Configuration

Model Configuration is where KeyRing AI shapes requests for specific providers and models. It is one of the most important parts of the product because modern AI providers do not all accept the same options, even when their APIs look similar at a high level.

![Model Configuration](../assets/screenshots/model-configuration.png)

_Public screenshot: Model Configuration with provider/model selection, profiles, quick toggles, live JSON summary, and per-model request controls._

A safe AI workspace cannot assume that every model supports temperature, top-p, JSON schema output, tool choice, stop sequences, log probabilities, reasoning controls, cache hints, retrieval settings, or streaming in the same way. KeyRing AI treats model configuration as a policy layer: choose the intended behavior, then send only the settings that make sense for the selected provider and model.

## Configuration Scope

Model settings can be reviewed by provider and model. This lets one model use conservative defaults while another model is tuned for creative writing, structured JSON, long-form drafting, tool use, retrieval, or deterministic evaluation.

The configuration surface is intentionally broad because provider capability is broad. A team evaluating models may need simple controls on one day and deeper request shaping the next. KeyRing AI keeps those controls in one place instead of spreading them across unrelated screens.

## Major Configuration Areas

Overview settings cover model identity, system prompt behavior, token limits, timeout expectations, and general request shape.

Decoding settings cover sampling behavior such as temperature, top-p, top-k, min-p, typical-p, penalties, and related controls where a provider supports them.

Beam and n-best settings support providers or models that expose alternative-generation controls.

Output control settings cover response format, stop sequences, JSON schema, grammar-like constraints, and structured-output expectations.

Tools and routing settings cover tool choice, tool availability, and provider/model behavior when external capabilities are enabled.

Retrieval settings cover search or RAG-style request options where the selected provider and workflow support them.

Performance settings cover streaming, cache hints, batching, speculative behavior, and latency-sensitive request preferences where available.

Logging and transport settings cover metadata and request-handling options that are appropriate for local evaluation.

## Profiles And Presets

KeyRing AI includes named profiles for common patterns such as precise question answering, strict JSON output, creative drafting, long-form writing, deterministic evaluation, tool-agent behavior, and cited retrieval workflows. Profiles are starting points, not universal truth. The right profile depends on the provider, model, prompt, and risk tolerance of the task.

The app also supports import and export of model configuration JSON so teams can move known-good settings between environments. Review imported configuration before use, especially if it came from outside your organization.

## Unsupported Settings

Unsupported settings should be omitted, not forced. This is a central rule. A model may use a provider-defined default for a parameter it does not expose. Sending the parameter anyway can produce avoidable errors.

For example, some newly released reasoning or flagship models may reject temperature or ignore sampling controls. In that case, the correct behavior is to let the model use its provider default rather than trying to coerce the older setting into the request.

This is why Model Discovery and Model Configuration work together. Discovery can make the model selectable. Configuration and policy determine how to call it safely.

## Recommended Workflow

Start from the provider's default behavior. Send a simple prompt without tools or attachments. If the model works, add one configuration change at a time. Use strict JSON or schema controls only when the model and provider support them. Use deterministic settings only when the provider exposes the relevant controls. Use tool settings only after the same model works without tools. Export a stable configuration once it has been validated.

## Evaluator Notes

When comparing two models, keep configuration as similar as the providers allow, but do not pretend that every provider has identical semantics. If one provider rejects a setting, remove it for that model and record the difference. The goal is reliable comparison, not artificial uniformity.

Metrics and history can help evaluate the impact of settings by showing latency, token counts, estimated costs, errors, and output quality over repeated runs.

## Public Boundary

This document describes the public purpose and operation of model configuration. It does not include proprietary request-shaping code, internal policy tables, provider secrets, source paths, or private debugging procedures.
