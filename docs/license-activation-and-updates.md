# License Activation And Updates

KeyRing AI has two connected product surfaces: the commercial website and the desktop app. The website manages account, license, download, and update workflows. The desktop app is where users run local AI workflows with their own provider keys.

## License Activation

License activation confirms that the desktop app is authorized for the user and machine. The activation flow is separate from provider API access. A valid KeyRing AI license allows the desktop product to run; provider keys and provider account permissions determine which AI providers and models can actually be used.

If activation fails, verify the license value, account state, network connectivity, system time, and whether the license is already associated with another machine or requires support action.

## Feature Tiers

Product tiers can affect which KeyRing AI workflow surfaces are available. Provider account tiers separately affect model access, quotas, billing, and provider-specific features. Both layers matter.

For example, a KeyRing AI tier may enable a multi-provider workflow while a provider account may still deny a specific model because the provider has not enabled it for that account.

## Updates

Desktop updates keep the app aligned with provider changes, model releases, workflow improvements, and reliability fixes. Users should keep the app current, especially when using newly released models or provider features.

The update system is part of the commercial trust boundary. It should be used through the product's normal update flow rather than by manually replacing internal files.

## Provider Changes And Updates

AI providers change quickly. A provider may release a new model, retire an older model, alter parameter support, change pricing, or update API behavior. Some changes can be handled through Model Discovery or Model Configuration. Others may require a KeyRing AI update.

When a newly released model appears through discovery but fails at runtime, test account access and unsupported parameters before assuming the desktop app is outdated.

## Troubleshooting

For license issues, check account and license state first. For provider request issues, check provider keys, model access, and provider dashboard status. For update issues, use the app's update surface and avoid manual file changes unless support directs it.

When reporting an issue, include the app version, license tier if relevant, workflow, provider/model involved, visible error, and whether the issue reproduces with a minimal prompt. Do not send provider keys, secrets, private customer data, or confidential attachments.

## Public Boundary

This document describes public activation and update behavior. It does not include private signing keys, internal entitlement implementation, deployment configuration, source paths, or infrastructure details.
