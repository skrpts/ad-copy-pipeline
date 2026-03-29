---
type: prompt
id: ad-copy-generator
title: Ad Copy Generator
description: "Creates platform-specific ad copy with character limits"
tags: [Customer-Facing]
connections:
  - target: llm-service
    type: runs_on
  - target: brand-voice-guide
    type: references
---

### Inputs

- **Key messages:** {{input.key_messages}}
- **Platform constraints:** {{input.platform_constraints}}
- **Audience segment profiles:** {{steps.audience-segmentation.output}}

Use the segmentation output — including demographics, psychographics, and preferred channels — to target the copy appropriately. Apply the platform constraints provided to set appropriate character limits for headlines and descriptions.

## Constraints
- Respect the platform-specific character limits provided in the platform constraints input
- Must include a clear CTA

## Brand Voice
Derive the brand voice from the key messages and customer data context.

Provide 5 variants with different angles (benefit-led, problem-solution, social proof, urgency, curiosity).
