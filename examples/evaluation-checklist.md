# Evaluation Checklist

Use this checklist when evaluating KeyRing AI with real providers. It is designed to produce useful results without exposing confidential data or confusing provider issues with KeyRing AI workflow issues.

## Before You Start

Confirm that you have an active KeyRing AI license, at least two provider accounts if you plan to compare models, provider billing or credits enabled, and approval to use the selected providers for the data you will test.

Use non-sensitive public or synthetic prompts for the first pass. Do not begin evaluation with customer data, credentials, regulated information, or private source code.

## Baseline Provider Test

Configure one provider key in API Settings. Send a short prompt to one known model with no tools, no attachments, no forced output format, and default model settings. Confirm that the response succeeds.

Repeat the same baseline test for each provider you plan to evaluate. Record failures separately from quality judgments.

## Model Discovery Test

Run Model Discovery for each provider that supports it. Save the provider configuration. Confirm that discovered models appear in the expected model picker or provider mode. Test newly discovered models with conservative defaults before applying advanced settings.

## Workflow Test

Run the same prompt across providers using provider tabs. Then run a Chatroom or Roundtable workflow if multi-model conversation is part of the evaluation. Keep the prompt stable so differences are easier to interpret.

## Metrics Review

Open Metrics and review latency, token counts, status, provider/model breakdowns, and estimated cost. Treat cost as directional until reconciled with provider billing data.

## Decision Notes

For each model, record output quality, speed, cost, reliability, access constraints, context handling, tool compatibility, structured-output support, and provider policy considerations.

## Public Boundary

This example contains no proprietary source code, private prompts, internal infrastructure details, or customer data.
