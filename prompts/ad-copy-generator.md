---
type: prompt
id: ad-copy-generator
title: Ad Copy Generator
description: "Creates platform-specific ad copy with character limits"
tags: [Customer-Facing]
connections:
  - target: llm-service
    type: runs_on
  - target: brand-voice-guidelines
    type: references
---

Write ad copy for {{platform}} targeting {{audience_segment}}. The goal is {{campaign_goal}}.

## Constraints
- Headline: max {{headline_chars}} characters
- Description: max {{description_chars}} characters
- Must include a clear CTA

## Brand Voice
{{brand_voice}}

## Key Messages
{{key_messages}}

Provide 5 variants with different angles (benefit-led, problem-solution, social proof, urgency, curiosity).
