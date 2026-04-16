# Runtime Boundaries

This document describes KeyRing AI's public runtime boundaries. It is written for customers, developers, and evaluators who want to understand what parts of the product are responsible for what work.

## Boundary Summary

KeyRing AI separates five major responsibilities:

1. Desktop app launch and local runtime supervision
2. Local AI workflow orchestration
3. User-facing desktop workspace
4. Website commercial trust flows
5. Third-party AI provider execution

Keeping these responsibilities separate is a core part of the product's trust model.

## Normal AI Request Boundary

For routine prompt execution, the public model is:

```text
User -> KeyRing AI desktop app -> selected AI provider
```

The selected AI provider receives the prompt, files, or generated context that the user sends to that provider. The KeyRing website is not the routine relay for that prompt path.

## Commercial Trust Boundary

The website participates in product trust and delivery flows such as:

- Account access
- License status
- Download access
- Update availability
- Support and documentation

These flows are separate from normal provider prompt execution. A desktop license check is not the same thing as sending a customer prompt through KeyRing's servers.

## Provider Account Boundary

The user's provider account remains authoritative for provider-side behavior:

- Model availability
- Model deprecations
- Billing and credits
- Rate limits
- Provider outages
- Provider error messages
- Provider data handling terms

KeyRing can organize and route provider usage, but it does not control a provider's account policy, pricing, retention rules, or model access decisions.

## Local State Boundary

The desktop app treats workflow state as a local application concern. Public examples include:

- Provider settings
- Model selections
- Conversation history
- Usage summaries
- Attachments and generated assets
- Export workflows

Local-first architecture does not mean data never leaves the device. If the user sends prompt content, files, or context to a provider, the selected provider receives that data.

## Native Capability Boundary

Native desktop capabilities are treated as higher-risk than ordinary text generation. Public examples include:

- Opening local files or folders
- Handling attachments
- Managing generated assets
- Starting desktop update flows
- Interacting with operating-system capabilities

The public design posture is that native capabilities should be scoped, intentional, and separate from generic provider text completion.

## Boundary Evaluation Checklist

When evaluating KeyRing AI, ask:

- Is this flow part of normal AI prompt execution, or part of commercial trust?
- Which provider receives this prompt or attachment?
- Which provider account controls model access and billing?
- Is the data staying in local workflow state, being exported, or being sent to a provider?
- Is the action a native desktop capability that deserves extra care?

## What This Document Avoids

This public document intentionally avoids exact token flows, private configuration names, source paths, implementation internals, private audit findings, and low-level security control descriptions.
