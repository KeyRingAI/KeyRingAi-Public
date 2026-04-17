# Public Workflow Examples

This folder documents public KeyRing AI workflows. The examples are intentionally documentation-first: they show how a customer or evaluator can reason about the product without copying proprietary application source code.

Do not add private app files, internal business logic, deployment configuration, secrets, customer data, or infrastructure details to this folder.

## Example 1: Configure A First Provider

Goal: connect one AI provider and confirm the desktop app can send a prompt.

Steps:

1. Open KeyRing AI and activate your license if prompted.
2. Open API Settings.
3. Choose a provider you already have an account with.
4. Open that provider's official dashboard and create a new API key.
5. Save the key in the matching KeyRing provider card.
6. Select a model that your provider account can access.
7. Enable the provider in the workspace.
8. Send this test prompt:

```text
Reply with one sentence confirming which provider and model are responding.
```

Expected result: the provider tab returns a response. If it does not, verify provider billing, quota, selected model access, and key validity in the provider dashboard.

## Example 2: Compare Multiple Providers

Goal: use KeyRing AI as a comparison workspace instead of switching between provider websites.

Steps:

1. Configure at least two providers.
2. Enable both providers in the Chatroom workspace.
3. Use a prompt that benefits from comparison:

```text
Compare two ways to reduce onboarding friction for a desktop AI product. Give tradeoffs, risks, and a final recommendation.
```

Expected result: each enabled provider answers in its own response surface, letting you compare tone, completeness, latency, and reasoning quality.

Good evaluation dimensions:

- Accuracy
- Specificity
- Latency
- Cost profile
- Ability to follow constraints
- Fit for the user's workflow

## Example 3: Use Model Discovery Before Routing

Goal: sync a provider's current model list before mapping product modes to models.

Steps:

1. Open Provider Manager.
2. Select a provider.
3. Run Model Discovery or Sync.
4. Review the discovered model list.
5. Save the discovery result.
6. Map provider modes such as Default, Reasoning, Vision, Image, or Video to models that exist in the saved inventory.
7. Return to the workspace and test the mapped mode.

Expected result: newly discovered and saved models become available for use where the provider account and KeyRing policy layer support them.

Important limitation: a model can appear in provider discovery while still being unavailable to a specific provider account because of billing, region, allowlist, deprecation, or quota rules.

## Example 4: Evaluate A Reasoning Model Safely

Goal: use a reasoning-capable model without assuming every provider accepts the same controls.

Steps:

1. Confirm the model is available to your provider account.
2. Save the model through Model Discovery if it was newly released.
3. Map the provider's Reasoning mode to that model where appropriate.
4. Start with provider defaults before adding advanced settings.
5. Send a prompt that benefits from deeper analysis:

```text
Review this launch checklist for missing risk controls. Group findings by severity and give a practical next-action list.
```

Expected result: the reasoning model may take longer and may use different token accounting than ordinary chat models.

If the provider rejects a setting, remove unsupported controls such as temperature or effort values and let the provider default apply.

## Example 5: Scope Attachments Deliberately

Goal: understand that local-first does not mean providers never receive data.

Steps:

1. Attach a non-sensitive test document.
2. Choose whether the attachment should apply globally or only to specific providers.
3. Use a prompt that references the attachment:

```text
Summarize the attached document in five bullets and identify any missing assumptions.
```

Expected result: only the selected providers should receive the context needed for the request.

Safety rule: do not send secrets, customer data, regulated data, or proprietary source code to a provider unless that provider and workflow are approved for that data.

## Example 6: Troubleshoot A Provider Error

When a provider tab fails, use this order:

1. Confirm the provider is enabled in KeyRing.
2. Confirm the selected model exists in the saved inventory.
3. Confirm the provider account has access to that model.
4. Confirm billing or credits are active in the provider dashboard.
5. Regenerate the provider API key if authentication fails.
6. Remove advanced settings that the model may not support.
7. Retry with a short prompt to isolate account and model access from prompt complexity.

Most provider failures come from provider-side account state, model access, quota, billing, or unsupported parameters rather than the local workspace itself.

## Example Contribution Rules

Public examples may include:

- Text prompts
- Workflow walkthroughs
- Public screenshots with secrets removed
- Public provider setup checklists
- Public troubleshooting checklists
- Small example files only when they contain no customer data or proprietary material

Public examples must not include:

- Proprietary application source code
- Private repo history or copied private files
- Secrets, tokens, certificates, credentials, or `.env` files
- Customer data or private prompts
- Internal infrastructure details
- Internal API contracts that are not public product interfaces
- Exploit instructions, bypass procedures, or security-sensitive implementation details
