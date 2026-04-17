# Notifications And Status

KeyRing AI exposes status information throughout the desktop workspace so users can understand what the app is doing, what requires attention, and where to take corrective action.

Status is intentionally visible. Multi-provider AI workflows can fail for many reasons: missing keys, provider quota, unavailable models, unsupported parameters, network problems, long-running media jobs, cancelled requests, or license/update state. A useful workspace should show these states near the action that caused them.

## Header Status

The header surfaces application-level information such as version, provider readiness, feedback and issue links, export access, update state, and exit controls. Provider readiness indicators help users see whether any configured keys are available before starting a workflow.

## Provider Status

Provider tabs can show ready, thinking, streaming, completed, cancelled, and error states. They can also expose elapsed time, token information, copy/export controls, retry affordances, and settings paths. This makes the provider tab the first place to look when a specific model request fails.

## Update Status

The desktop app can check for updates and show update progress through the app interface. Users should keep the desktop app current, especially when providers release new models or change API behavior. Updates can include provider compatibility improvements, workflow fixes, and reliability changes.

## Long-Running Jobs

Media generation and some agent workflows may run longer than ordinary chat requests. KeyRing AI can show job progress, completion, failure, retry, preview, or cancellation states depending on the workflow.

For long-running jobs, avoid starting duplicate runs until the current job status is clear. Provider-side jobs may continue or bill according to provider rules even if the local workflow is interrupted.

## Feedback And Known Issues

Feedback and known-issue surfaces help users report product behavior without mixing it into provider troubleshooting. When reporting an issue, include the workflow, provider, model, visible error, and whether the problem occurs with a minimal prompt. Do not include API keys, secrets, customer data, or private attachments.

## Public Boundary

This document describes public status and notification behavior. It does not include internal telemetry implementation, private route names, deployment configuration, or security-sensitive monitoring details.
