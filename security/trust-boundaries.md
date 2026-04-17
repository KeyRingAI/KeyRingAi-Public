# Public Trust Boundaries

KeyRing AI is designed around clear trust boundaries between the website, desktop app, local runtime, AI providers, and user-controlled data. This document gives evaluators a public, high-level map without publishing implementation details.

## Website Boundary

The website supports commercial workflows such as account access, pricing, license state, downloads, updates, and support. It is separate from normal prompt execution. The website does not need routine prompt or response content to perform those commercial functions.

## Desktop Boundary

The installed desktop app is the user's AI workspace. It manages provider setup, model selection, prompt composition, local history, attachments, metrics, exports, Roundtable, Agent Builder, tool consent, and media workflows.

The desktop app should be operated through its supported interface and update path. Users should not expose local runtime components as public services.

## Provider Boundary

AI providers receive the prompts, attachments, and context the user chooses to send to them. Providers control model access, billing, quotas, retention, safety review, regional availability, and account policy. KeyRing AI helps route and organize provider usage, but it does not replace the provider relationship.

## Local Data Boundary

Workspace data is stored locally so users can review and control their work. Local history, exports, attachments, metrics, prompt presets, provider configuration, and generated assets should be treated as sensitive when the underlying work is sensitive.

## Tool Capability Boundary

Tool-enabled workflows can have effects beyond ordinary text output. KeyRing AI distinguishes tool capabilities from normal chat behavior and documents dangerous tool consent at a public level. Users should grant only the capabilities needed for the task.

## Public Boundary

This document does not disclose source code, exact security controls, token internals, private endpoint behavior, infrastructure diagrams, deployment configuration, exploit details, or internal audit findings.
