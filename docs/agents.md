# Agents

Agent Builder lets users create local AI workflows that combine a provider, model, role instructions, execution settings, memory behavior, and approved tools. It is intended for repeatable tasks that need more structure than a one-off prompt.

An agent in KeyRing AI is a configured workflow, not an autonomous cloud service. The desktop app remains the user-facing control point. Provider calls are made from the local app using the user's provider keys, and tool access is governed by the user's configuration and consent.

## Agent Types

KeyRing AI supports several agent patterns. A simple assistant is useful for direct task execution. A tool-oriented agent can call approved tools. A planner can break work into steps. A reflective agent can critique or revise its own output. Specialized templates can help users start with common patterns such as research assistant, code reviewer, data analyst, or creative writer.

Templates are starting points. Users should review the prompt, provider, model, tools, memory settings, and safety assumptions before running an agent on meaningful work.

## Builder Sections

Agent setup covers identity, provider, model, and general behavior.

Prompt settings define the role, task style, constraints, and expected output.

Tool settings define which capabilities the agent may use and whether tool use is automatic, required, or disabled.

Configuration settings cover memory, reasoning behavior where supported, fallback providers, and related execution preferences.

## Tools And Consent

Some tools are low risk, such as formatting or limited data processing. Others can be powerful, including file access, shell or code execution, package installation, network requests, image generation, or system-level actions. KeyRing AI requires explicit consent before dangerous tool categories are used.

Consent is not a formality. A tool-enabled agent can act on instructions, attachments, and model output. Users should only enable tools that are required for the task, review the agent's configuration, and monitor the run.

## Running And Reviewing Agents

Agent runs can show streaming output, tool calls, intermediate steps, status changes, completion, cancellation, and export options. Users should inspect both the final answer and the tool traces when tool use is involved. A plausible final answer is not enough if the agent used the wrong file, exceeded scope, or relied on weak evidence.

For important work, start with a small dry run using non-sensitive inputs. Add tools only after the model and prompt work without them. Keep fallback providers conservative, because switching providers can change model behavior and data handling terms.

## Safe Usage Guidance

Do not give an agent broad tool access for a vague objective. Do not include secrets in the prompt. Do not attach sensitive files unless the provider and workflow are approved. Prefer narrowly scoped tools, short runs, and explicit success criteria. Export results only after reviewing for sensitive content.

## Public Boundary

This document describes public agent workflow behavior. It does not include proprietary agent execution code, internal tool adapters, hidden prompts, private route names, or customer agent configurations.
