---
type: prompt
id: ad-copy-generator
title: Ad Copy Generator
description: "Creates platform-specific ad copy with character limits"
tags: [Customer-Facing, Writing, Audience]
inputs:
  key_messages:
    label: "Key Messages"
    description: "Core messages to communicate"
    example: "Save 10 hours/week on repetitive AI tasks. No code required."
    required: true
    type: text
  platform_constraints:
    label: "Platform Constraints"
    description: "Technical or platform constraints"
    example: "Must work on mobile web. No native app. 3G connection support."
    required: true
    type: text
connections:
  - target: audience-segmentation
    type: derived_from
  - target: llm-service
    type: runs_on
  - target: brand-voice-guide
    type: references
---

### Inputs

- **Key messages:** {{input.key_messages}}
- **Platform constraints:** {{input.platform_constraints}}
- **Audience segment profiles:** {{steps.Audience Segmentation.output}}

Use the segmentation output — including demographics, psychographics, and preferred channels — to target the copy appropriately. Apply the platform constraints provided to set appropriate character limits for headlines and descriptions.

## Constraints
- Respect the platform-specific character limits provided in the platform constraints input
- Must include a clear CTA

## Brand Voice
Derive the brand voice from the key messages and customer data context.

Provide 5 variants with different angles (benefit-led, problem-solution, social proof, urgency, curiosity).
