# Public Data Flows

This document summarizes KeyRing AI's public data-flow model at a customer-facing level. It is not an implementation specification.

## Normal Prompt Execution

A simplified normal prompt flow looks like this:

```text
1. User enters a prompt in the desktop workspace.
2. The local runtime prepares the provider request.
3. The local runtime applies the selected provider and model settings.
4. The request is sent to the selected AI provider.
5. The provider returns a response to the local runtime.
6. The desktop workspace displays, compares, stores, or exports the result.
```

The important public point is that normal prompt execution is desktop-to-provider. The website layer is not the standard prompt relay.

## Provider Model Discovery

Model Discovery is a provider maintenance workflow. A public-safe version of the flow is:

```text
1. User selects a provider in Provider Manager.
2. KeyRing queries the provider's available model inventory using the user's provider setup.
3. The user reviews discovered models.
4. The user saves the discovery result.
5. Saved models become available for provider selection and mode mapping where supported.
```

Provider Discovery does not guarantee that every discovered model can be used by every account. Provider-side access, billing, regional availability, deprecations, and rate limits still apply.

## Provider Mode Mapping

Provider modes help map product workflows to concrete models. Common public mode categories include:

- Default chat
- Reasoning
- Vision
- Image
- Video
- Deep research or search-oriented workflows where available

Not every provider supports every mode. Not every model in a mode accepts the same settings.

## Reasoning-Capable Models

Reasoning-capable models vary significantly across providers. Some accept explicit effort controls. Some use provider-specific fields. Some reject ordinary sampling controls. Some simply rely on provider defaults.

The public KeyRing design goal is to shape the request for the selected provider and model so that unsupported settings do not unnecessarily break the workflow. For example, if a model does not accept temperature, the safer behavior is to omit temperature and let the provider use its default.

## License And Update Flows

License and update flows are separate from routine prompt execution.

A public-safe summary:

```text
1. The desktop app checks entitlement or update information with the website layer.
2. The website responds with license or update status.
3. The desktop app uses that status to allow product access or present update availability.
```

These flows are about commercial trust and product delivery. They should not include customer prompt content.

## Attachments And Generated Assets

Files and generated assets are local workflow objects until the user takes an action that sends or exports them.

Examples:

- If a file is attached to a provider prompt, the selected provider may receive relevant file content.
- If a user exports a conversation or asset, the output goes where the user chooses.
- If a generated asset is produced by a provider, provider terms and data handling practices apply to that generation request.

## Errors And Provider Differences

Provider errors can originate outside KeyRing's control. Common causes include:

- Missing or invalid provider API key
- Insufficient provider account access
- Provider-side billing or quota limits
- Unsupported model parameter
- Deprecated model name
- Temporary provider outage

KeyRing's provider-aware orchestration can reduce avoidable mismatch errors, but it cannot override provider account policy or service availability.

## Documentation Boundary

This document avoids internal route names, private schemas, source paths, exact security controls, deployment details, secrets, customer data, and proprietary implementation logic.
