# Troubleshooting Provider Errors

Provider errors are common in multi-model workflows because each provider controls its own keys, billing, model access, request parameters, rate limits, and service availability. KeyRing AI helps organize the correction path, but the source of truth for provider account status remains the provider.

## Start With A Minimal Test

When a request fails, reduce the workflow to one provider, one model, one short prompt, no attachments, no tools, no forced response format, and default model settings. If the minimal test works, add features back one at a time until the failure returns.

This is the fastest way to separate provider access problems from prompt, attachment, tool, or configuration problems.

## Common Error Classes

Authentication errors usually mean the provider key is missing, invalid, revoked, copied incorrectly, or not authorized for API use. Check API Settings and the provider dashboard.

Billing or quota errors usually mean the provider account is out of credits, has no payment method, has hit a usage cap, or is rate limited. Resolve these in the provider dashboard.

Model access errors usually mean the model is not available to that account, region, tier, organization, or beta program. Discovery can list a model before the account can run it.

Unsupported parameter errors usually mean the selected model rejected one or more request settings. Open Model Configuration and remove settings the model does not support. Let provider defaults apply where appropriate.

Timeout and unavailable errors may be caused by provider service health, network conditions, unusually large prompts, long media jobs, or temporary provider instability. Retry with a smaller request before changing app configuration.

Empty or malformed response errors can indicate provider-side failure, incompatible output settings, tool-call mismatch, or a response shape the workflow did not expect. Test without tools and structured output first.

## Where To Fix The Problem

Use API Settings when the key, license, or provider credential state is wrong.

Use Provider Manager when a model is missing, mapped to the wrong mode, or needs discovery.

Use Model Configuration when a provider rejects request parameters or a model needs different defaults.

Use Attachments when a file is too large, wrongly scoped, or not included as expected.

Use the provider dashboard when the issue is billing, quota, account access, model entitlement, provider incidents, or organization-level permissions.

## Reporting A Problem

When asking for support, include the provider name, model name, workflow, visible error text, whether a minimal prompt works, and the approximate time of the failure. Do not include API keys, secrets, private attachments, customer data, or confidential prompts.

## Public Boundary

This document describes public troubleshooting behavior. It does not include internal error-mapping code, private diagnostics, provider credentials, source paths, or implementation details that could weaken the product.
