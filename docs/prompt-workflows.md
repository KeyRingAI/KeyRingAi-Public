# Prompt Workflows

The prompt panel is the starting point for most KeyRing AI work. It is where the user writes the request, adds optional system context, chooses providers and models, enables workflow options, and decides whether the request should run as a direct provider call, Chatroom interaction, Roundtable input, tool-enabled task, or agent-driven workflow.

## Prompt Composition

A good KeyRing AI prompt should make the task, context, constraints, and expected output explicit. Because the same prompt may be sent to more than one provider, avoid relying on provider-specific wording unless you are intentionally testing that provider.

For comparison work, keep the prompt stable across providers and change one variable at a time. For production work, keep sensitive context out of prompts unless your organization has approved the selected provider for that data.

## System Context

System context can guide tone, role, format, and constraints. It is powerful, but it should be used deliberately. Overly broad system context can make model comparison harder because it hides whether the provider or the instruction caused a change in behavior.

Use short, direct system context for routine tasks. Use more detailed system context for agent workflows, structured analysis, or compliance-sensitive review where the model must follow a specific operating frame.

## Request Options

KeyRing AI exposes workflow options that can change how a prompt is routed and displayed. These can include streaming responses, routing output to Chatroom, using model mentions, enabling tool calling, using agent execution, and enabling deliberation or consensus-style behaviors where available.

Do not enable every option by default. Add options as the task needs them. A plain provider request is easier to diagnose than a complex tool-enabled, attachment-heavy, multi-provider workflow.

## Provider Modes

Providers and models can be organized by mode, such as default chat, reasoning, vision, image, video, or research-oriented workflows. The selected mode determines which models and settings make sense for the task.

A model should be used in a mode that matches its capability. If a model is discovered but appears in the wrong place, review Provider Manager and Model Discovery mappings before treating the provider as broken.

## Model Mentions

Model mentions let users direct attention to particular models in workflows that support them. They are useful when a user wants one model to answer, another to critique, and a third to synthesize, or when a prompt should be routed to a specific provider participant.

Use mentions clearly and sparingly. A prompt full of ambiguous model references is harder to audit later in History.

## Workflow Examples

For quick comparison, select two providers, disable tools and attachments, send the same prompt, and compare provider tabs.

For collaborative analysis, enable Chatroom or Roundtable, choose participants, provide a topic, and export the transcript after review.

For structured output, choose a model that supports the needed output controls, configure Model Configuration conservatively, and validate the output before relying on it.

For context-heavy work, add attachments with the narrowest useful ingestion mode and verify that only the intended provider receives them.

## Prompt Safety

Do not include provider API keys, passwords, private tokens, customer secrets, or confidential production data in prompts unless the selected provider and use case have been approved. Remember that if a prompt is sent to a provider, the provider receives it under that provider's terms.

## Public Boundary

This document covers public prompt workflow behavior. It does not disclose proprietary orchestration code, internal route names, hidden state structures, or private security logic.
