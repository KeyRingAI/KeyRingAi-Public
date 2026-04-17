# Prompt Presets

Prompt Presets help users turn repeatable prompt patterns into reusable workspace assets. Instead of rewriting the same instruction every time, users can save, tag, search, insert, export, import, and back up prompt templates.

Presets are useful for teams that evaluate models, repeat review workflows, maintain standard analysis patterns, or want consistent output formats across providers.

## What A Preset Contains

A preset typically includes a name, prompt text, and tags. The text can be inserted into the prompt editor when needed. Tags make it easier to group presets by task, provider, department, format, or review stage.

Presets should be written as reusable instructions, not as storage for secrets or case-specific confidential data. A good preset describes the work pattern and leaves sensitive context to be added only when the provider and task are approved.

## Built-In And User Presets

KeyRing AI can include built-in prompt templates as examples or starting points. Users can also create their own saved presets. Built-ins are useful for onboarding; user presets are where teams capture their own working style.

When building a preset library, keep names short and descriptive. Tags should help retrieval, not become a second title. For example, a preset named "Contract Risk Summary" might use tags such as legal, summary, risk, and structured-output.

## Using Presets In Workflow

Open Prompt Presets, search or filter by tag, choose a preset, and insert it into the prompt editor. Then add the task-specific context. If the preset expects a particular output format, confirm that the selected model supports the needed response controls.

Some workflows may support preset references from the prompt editor. Even when that is convenient, users should review the expanded prompt before sending it to a provider.

## Backups, Export, And Import

Prompt libraries become valuable over time, so KeyRing AI supports backup and import/export workflows. Use exports to share approved prompt patterns across machines or teams. Use backups before major cleanup or reorganization.

Review imported presets before use. A preset imported from another source may contain hidden assumptions, outdated provider instructions, sensitive text, or a format that does not match the current model.

## Preset Quality Checklist

The preset has a clear name. The instruction is reusable and does not contain secrets. The expected output format is stated. The tags make the preset easy to find. The preset works with more than one provider unless intentionally provider-specific. The preset has been tested with a simple non-sensitive example.

## Public Boundary

This document describes public prompt-preset behavior. It does not include private prompt libraries, proprietary templates, internal storage details, or customer data.
