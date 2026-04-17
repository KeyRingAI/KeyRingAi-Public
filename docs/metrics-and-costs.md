# Metrics And Costs

Metrics Intelligence helps users understand how KeyRing AI workflows use providers and models. It is designed for local evaluation, operational awareness, budgeting, and troubleshooting.

Metrics are especially useful when a team is comparing models across cost, latency, token usage, error rate, and output usefulness. A model that gives a strong answer may still be unsuitable for a workflow if it is too slow, too expensive, unavailable too often, or inconsistent under the required settings.

## What Metrics Can Show

The metrics surface can show request-level records, session-level summaries, provider and model breakdowns, token counts, estimated costs, latency, status, and related event information. It can also support filters by timeframe, provider, model, cost state, event type, or search text.

This gives users a way to answer practical questions: which providers are used most often, which models are slowest for a workflow, which requests failed, which model settings changed cost or latency, and which sessions should be exported for deeper review.

## Cost Estimates

Cost values should be treated as estimates unless reconciled against provider billing records. Providers can change pricing, apply discounts, count tokens differently, bill for cached tokens differently, or include separate charges for tools, media, retrieval, storage, or premium features.

KeyRing AI's metrics are useful for directional analysis. Provider dashboards and invoices remain the source of truth for actual billing.

## Recalculation And Export

Metrics can be recalculated when pricing metadata or records need to be refreshed. Users can export metrics in common analysis formats for spreadsheet review, reporting, or internal evaluation.

When exporting metrics, remember that records may reveal provider usage patterns, prompt topics, model names, costs, or session structure. Treat exports as internal operational data unless reviewed and approved for sharing.

## Reset And Retention

Users may reset or clear local metrics when the data is no longer needed or when starting a fresh evaluation. Resetting local metrics does not change provider-side billing history.

For serious evaluations, export a snapshot before resetting. This preserves evidence for later comparison while keeping the active local workspace clean.

## Evaluation Workflow

Start with a baseline prompt and one provider. Run the same prompt across the providers being evaluated. Review latency, status, tokens, and estimated cost. Change only one model setting at a time. Export the metrics and compare them with qualitative review of the actual responses. Repeat with realistic prompts after the setup is stable.

## Public Boundary

This document explains public metrics behavior. It does not include proprietary pricing implementation, database internals, private source paths, customer records, or confidential usage data.
