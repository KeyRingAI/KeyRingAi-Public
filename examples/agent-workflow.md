# Agent Workflow Example

This example shows a conservative way to test an agent before granting broader capabilities.

## Goal

Create a research-style agent that summarizes public information and produces a structured review.

## Setup

Open Agent Builder. Start with a research assistant template or a simple assistant pattern. Select one provider and model that already passes a direct prompt test. Write a narrow role prompt that defines the task, output format, and limits.

## Tools

Start with tools disabled. Run a simple test. If the agent needs tools, enable only the specific tool category required for the task and review the dangerous-tool consent prompt carefully.

## Run

Use a public or synthetic input. Watch the run status and any tool-call trace. Stop the run if it moves outside the intended task.

## Review

Inspect the final answer and any tool activity. Export only after checking for sensitive material.

## Public Boundary

This example does not include proprietary agent implementation, private prompts, internal tool adapters, customer data, or credentials.
