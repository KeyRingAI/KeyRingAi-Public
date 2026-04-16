# Public Trust Boundaries

This document gives a public, non-sensitive overview of how KeyRing AI separates security responsibilities. It is designed for customer evaluation and developer understanding, not as an implementation guide.

## Boundary Summary

KeyRing AI is built around separate trust zones:

1. Website commercial trust
2. Desktop launch and local runtime trust
3. Desktop interface to local runtime trust
4. Local runtime to AI provider trust
5. Local secret and user-data handling
6. Native capability and automation boundaries

The product's core security goal is to keep these zones understandable and separate.

## 1. Website Commercial Trust

The website supports account, license, download, update, and support workflows.

This layer can confirm whether a user is entitled to use the product, but it is not the routine chat relay for provider prompts and model responses.

## 2. Desktop Launch And Local Runtime Trust

The desktop app launches and supervises its local runtime. This local runtime is part of the desktop product and is not intended to behave like a public web service.

The public design objective is to keep desktop runtime startup bounded, local, and controlled by the app.

## 3. Desktop Interface To Local Runtime Trust

The frontend workspace communicates with the local runtime through a local session boundary. The product is designed so normal desktop controls do not depend on exposing a broad remote API surface.

The public design objective is to keep local application communication local and scoped.

## 4. Local Runtime To AI Provider Trust

When users enable providers, KeyRing AI uses their provider configuration to communicate with the selected provider.

The user's provider account remains the source of truth for:

- Model availability
- Billing and credits
- Rate limits
- Provider-side errors
- Provider terms and data handling

The public design objective is direct provider usage without turning KeyRing's website into a prompt middleman.

## 5. Local Secret And User Data Handling

Provider credentials, license state, conversations, files, and workflow state are treated as desktop-side concerns.

The public design objective is to avoid centralizing provider credentials in a shared KeyRing cloud vault for routine provider use.

Important limitation: local-first design does not remove the selected AI provider from the trust model. If a prompt, attachment, or generated context is sent to a provider, that provider receives it.

## 6. Native Capability And Automation Boundaries

Native desktop capabilities are treated differently from plain text chat because they may affect the user's machine or external services.

Public design objectives include:

- Keep native actions scoped.
- Avoid broad arbitrary local execution surfaces.
- Treat filesystem and network automation as sensitive.
- Keep secrets out of contexts that do not need them.
- Review automation features separately before describing them as production-ready behavior.

## What This Public Document Avoids

This document intentionally avoids exact implementation details such as internal token flows, configuration names, route internals, port rules, private audit findings, or control-specific bypass discussion.

That restraint is intentional: the public repo should build trust without becoming a security playbook for attackers.
