# Tools And Consent

Tools extend model workflows beyond text generation. They can help an agent inspect files, process data, run controlled operations, generate media, call network resources, or interact with provider-native capabilities. Because tools can change the risk profile of a workflow, KeyRing AI treats consent and scope as first-class product concepts.

![Settings and tool consent](../assets/screenshots/settings.png)

_Public screenshot: Settings surface showing desktop preferences and dangerous tool consent status._

## Why Consent Matters

A normal prompt asks a model to produce text. A tool-enabled workflow may allow the model or agent to request an action. Depending on the tool, that action may read local files, write output, run code, make network requests, install dependencies, create generated media, or interact with a connected service.

KeyRing AI surfaces explicit consent for dangerous tool categories so users understand the difference between asking for advice and allowing an AI-driven workflow to operate in the local environment.

## Tool Categories

Tools can include web and internet capabilities, file-system workflows, code execution, image or media generation, system-related actions, and data-processing utilities. Availability depends on the configured provider, selected model, license tier, local settings, and user consent.

Provider-native tools and local tools should be treated differently. Provider-native tools run under the provider's platform and terms. Local tools operate from the desktop environment and may interact with local resources. Users should understand which category is being used before enabling a workflow.

## Practical Consent Model

Consent should be specific to the task. If an agent only needs to summarize a document, it should not need broad shell access. If a workflow only needs metadata, it should not receive raw file contents. If a provider can answer without a tool, test that path first.

Users should review the tool list, provider/model selection, prompt instructions, active attachments, and run objective before approving dangerous tools. Consent can be revoked or avoided by disabling the relevant tool access and running the workflow in a narrower mode.

## Safe Operating Practices

Use the minimum tool set required for the job. Start with non-sensitive data. Keep runs small until the prompt and model behavior are understood. Monitor tool calls during execution. Review generated files or commands before relying on them. Stop a run if it leaves the intended scope.

Do not place credentials, private tokens, provider keys, certificates, or production secrets in prompts, attachments, presets, or tool instructions. A model with tool access can be influenced by the content it sees.

## Public Boundary

This document explains the public tool-consent model at a high level. It does not disclose internal sandbox implementation, bypass details, proprietary tool adapters, security-sensitive configuration, or private test procedures.
