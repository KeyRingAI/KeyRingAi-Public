# History And Exports

KeyRing AI stores conversation history locally so users can review prior work, reload sessions, compare provider output, export selected records, and delete records that are no longer needed. History is a workspace feature, not a cloud sync service.

## What History Captures

History can include prompts, provider responses, selected providers and models, timestamps, status, token information, cost estimates, tool traces or media references where applicable, and workflow metadata needed to reload or inspect a session.

This makes History useful for model evaluation and audit-style review. It also means users should treat local history as sensitive if prompts or outputs contain sensitive material.

## Finding Prior Work

The History view supports search, filters, and sorting. Users can narrow results by status, mode, provider, time, token usage, cost, prompt text, or similar criteria depending on the available record data.

A practical pattern is to search by project or prompt phrase, filter down to completed runs, then sort by time or cost. This helps identify the version of a session that should be loaded or exported.

## Loading And Reusing Sessions

Loading a prior session can restore useful context for continued work. Before sending a new prompt from a loaded session, review active providers, selected models, attachments, and request settings. A session created for one evaluation may not be appropriate for a later production task.

If a prior run used a model that is no longer available or whose provider behavior changed, rerun with conservative defaults before relying on the restored workflow.

## Export Options

KeyRing AI supports exporting individual records and broader history sets for review outside the app. Exported material may include prompt text, responses, metadata, and model/provider details.

Before sharing exports, inspect them for confidential prompts, attachment references, provider keys, customer data, internal project names, or model output that should remain private. Exports are useful, but they should be handled like work product.

## Deleting Local Records

Users can delete records that are no longer needed. Deleting local records affects local workspace history. It does not control what an external AI provider may retain under its own terms after receiving a prompt or attachment content.

For provider-side retention or deletion questions, consult the provider's documentation and account controls.

## Review Practices

Use clear prompt naming or consistent phrasing so history is searchable. Export important evaluation runs before resetting or cleaning local data. Avoid storing secrets in prompts or presets. Delete stale local records that no longer serve a business purpose. Reconcile metrics and exports against provider dashboards when cost or compliance decisions depend on exact numbers.

## Public Boundary

This document describes public history and export behavior. It does not include private storage internals, local filesystem paths, database schema, source code, or customer records.
