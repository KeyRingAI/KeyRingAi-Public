# Provider Error Triage

Use this example when a provider request fails.

## Step 1: Reduce The Request

Use one provider, one model, one short prompt, no attachments, no tools, no forced output format, and default model settings.

## Step 2: Classify The Error

Authentication errors usually belong in API Settings or the provider dashboard. Billing, quota, and model-access errors usually belong in the provider dashboard. Unsupported parameter errors usually belong in Model Configuration. Missing or wrongly mapped models usually belong in Provider Manager and Model Discovery.

## Step 3: Add Complexity Back

After the minimal prompt works, add streaming, then model settings, then attachments, then tools, then multi-provider workflows. Stop when the failure returns.

## Step 4: Report Cleanly

When asking for help, include provider, model, workflow, visible error, app version, and whether the minimal prompt works. Do not include API keys, secrets, private prompts, customer data, or attachments.

## Public Boundary

This triage example does not include private diagnostics, source code, internal error mapping, credentials, or customer data.
