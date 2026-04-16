# Provider Manager

Provider Manager is KeyRing AI's provider maintenance surface. It is used to inspect provider records, sync model inventories, map provider modes to concrete models, and adjust provider display details.

This document describes public product behavior only. It does not expose proprietary registry implementation details.

For the higher-level provider architecture, see [Provider Orchestration](provider-orchestration.md). For reasoning-capable models, see [Reasoning Models](reasoning-models.md).

## What Provider Manager Does

Provider Manager helps with:

- Selecting a provider to inspect or maintain
- Syncing model inventory through model discovery
- Reviewing discovered models
- Mapping routing modes to specific models
- Adjusting provider visual identity
- Saving provider maintenance changes

It is a control-plane surface, not the normal day-to-day prompt workflow.

## Layout

The public UI model has three working areas:

### Left Column

- Provider list
- Provider search input
- Model-count summary per provider

### Center Column

- Selected provider header
- Sync controls
- Save controls
- Routing controls
- Visual identity controls

### Right Column

- Model count
- Model search
- Capability filters
- Model preview list

## Syncing Models

A typical model sync flow:

1. Select the provider.
2. Click Sync.
3. Review the discovered model list.
4. Review model categories or capability filters where available.
5. Click Save to persist the sync result.

Discovery results are not durable until saved.

After a model inventory is saved, KeyRing can use the saved inventory together with provider mode mappings and model policy rules to make the model available where it is supported.

## Routing Controls

Routing controls map KeyRing AI provider modes to concrete provider models.

Common routing targets include:

- Default
- Reasoning
- Image
- Vision
- Video

Each routing target should point to a model that exists in the provider's current inventory and is available to the user's provider account.

## Visual Identity

Provider Manager can expose provider display settings such as:

- Tab color
- Text color
- Color picker input
- Hex field input

These settings affect how a provider appears in the desktop UI.

## Important Scope Notes

Provider Manager is a maintenance surface. Public behavior may include limitations such as:

- Editing existing provider entries rather than exposing a full public provider-creation console.
- Requiring saved model inventory before routing mappings can be useful.
- Showing a preview list that may not render every model at once.
- Falling back to read-only provider data if the registry control plane is unavailable.
- Relying on the user's provider account for final model access, quota, billing, and region eligibility.

## Recommended Workflow

1. Select the provider you want to maintain.
2. Sync the model list.
3. Review discovered models.
4. Save the discovery result.
5. Set or update mode mappings.
6. Adjust visual identity only if needed.
7. Save changes.
8. Return to the main workspace and verify the provider behaves as expected.

## Troubleshooting

- **Synced models did not stick:** click Save after reviewing the sync result.
- **Cannot find every model in the visible panel:** use search and filters; large inventories may be previewed rather than fully displayed at once.
- **Selected model does not work:** your provider account may not have access to that specific model, or the provider may reject a setting for that model.
- **Reasoning model rejects a setting:** use provider defaults or remove unsupported advanced controls.
- **Provider appears unavailable:** confirm your license tier, provider key, billing, selected model, and active provider state.
