# Model Discovery Checklist

Use this checklist when a provider releases a new model or when the local model list appears out of date.

## Discovery Steps

Open Provider Manager. Select the provider. Confirm that the provider key and base configuration are valid. Run Model Discovery. Review the discovered list. Check that the model appears under the expected mode, such as chat, reasoning, image, video, vision, or research. Save the provider configuration.

## Runtime Test

Select the newly discovered model in a simple workflow. Send a short prompt with no tools, no attachments, no forced response format, and default model settings.

If the provider rejects a parameter, open Model Configuration and remove unsupported settings for that model. Let the provider default apply where appropriate.

If the provider denies access, verify account eligibility, billing, region, beta status, and quota in the provider dashboard.

## Review Notes

Record the discovered model name, provider, mode mapping, account access status, working settings, unsupported settings, and any provider-side requirements.

## Public Boundary

This checklist does not disclose proprietary model policy code, internal provider adapters, private source paths, or credentials.
