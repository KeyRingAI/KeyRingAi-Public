# Local Runtime Safety

KeyRing AI uses a desktop runtime model so the user's AI work happens from the local machine instead of through a hosted prompt relay. This public document explains the safety posture at a high level without publishing implementation details that would weaken the product.

## Runtime Boundary

The desktop app owns the user-facing experience and supervises the local runtime used for workspace functions. The local runtime is part of the desktop application. It is not intended to behave like a public internet API.

This boundary matters because provider keys, prompts, attachments, local history, exports, metrics, and workflow settings are handled on the user's device. The local runtime should be treated as part of the local app trust boundary, not as a service to expose broadly.

## Session And Request Discipline

State-changing desktop actions should be performed through the app's normal session controls. Users should not attempt to script or expose the local runtime as a public service. Doing so can bypass the product's intended operating assumptions and may create data exposure risk.

For normal use, operate KeyRing AI through the installed desktop interface and update through the product's supported update flow.

## Native Capabilities

Some desktop actions interact with native capabilities such as local files, generated assets, clipboard-like workflows, external openings, or automation-style tools. These capabilities are useful, but they should be scoped to the task and reviewed before use.

Users should avoid giving AI-driven workflows broad local access for vague objectives. Tool-enabled workflows deserve extra attention because they can have side effects beyond ordinary text generation.

## Public Boundary

This document is intentionally high-level. It does not disclose exact process controls, token internals, startup details, private endpoint behavior, sandbox internals, bypass narratives, or security test procedures.
