# Text To Speech

Text-to-speech features help users review model output by listening instead of reading. This is useful for long answers, Roundtable transcripts, Chatroom dialogue, accessibility preferences, and workflows where hearing multiple model voices improves review.

Voice features are optional. They depend on local configuration and, when using a third-party voice provider, the user's account, key, quota, and provider terms.

## Basic Playback

Provider responses can expose speak and stop controls where text-to-speech is available. A user can play back a response, stop playback, and continue reviewing the written answer in the same workspace.

Text-to-speech should be treated as a review aid. The written answer remains the source that should be copied, exported, or audited.

## Voice Provider Setup

KeyRing AI can be configured with a voice provider key for higher-quality speech workflows. Users should treat voice provider keys like other API credentials. Do not paste them into prompts, presets, shared screenshots, or public issues.

Voice provider availability, pricing, rate limits, voices, and usage rights are controlled by the provider. Review provider terms before using generated speech commercially or with sensitive content.

## Chatroom And Roundtable Voices

Voice playback becomes especially useful in Chatroom and Roundtable workflows because different providers or participants can be assigned recognizable voices. This can make long multi-model conversations easier to follow.

Assigned voices are a convenience feature. They should not be treated as identity verification, authorship proof, or a guarantee that a model's answer is correct.

## Sensitive Content Guidance

If a response contains confidential information, regulated data, customer material, or private business context, consider whether it should be sent to an external voice provider for synthesis. The fact that text was already produced by one AI provider does not automatically mean it should be sent to another.

Use local or lower-risk review paths when the text is sensitive and voice playback is not essential.

## Public Boundary

This document describes public text-to-speech behavior. It does not include proprietary audio implementation, private provider credentials, internal storage paths, or customer audio.
