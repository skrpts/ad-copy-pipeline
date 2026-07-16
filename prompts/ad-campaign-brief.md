---
type: prompt
id: ad-campaign-brief
title: "Ad Campaign Brief"
description: "Collects campaign details and target audience for ad copy generation"
tags: [Production]
inputs:
  product_name:
    label: "Product or Service"
    description: "What you are advertising"
    example: "CloudSync Pro — team file sharing and collaboration"
    required: true
    type: text
  target_audience:
    label: "Target Audience"
    description: "Who you want to reach"
    example: "Small business owners, 10-50 employees, not technical"
    required: true
    type: text
  campaign_objective:
    label: "Campaign Objective"
    description: "What this campaign should achieve"
    example: "Drive free trial sign-ups"
    required: true
    type: text
  key_messages:
    label: "Key Messages"
    description: "Core messages or value propositions"
    example: "Simple setup, no IT needed, 14-day free trial"
    required: false
    type: text
connections:
  - target: audience-segmentation
    type: derived_from
metadata:
  output_format: markdown
  prompt_type: task
---

You are an advertising strategist. Analyze the target audience for this ad campaign and produce audience segments.

**Product:** {{input.product_name}}
**Target audience:** {{input.target_audience}}
**Objective:** {{input.campaign_objective}}
**Key messages:** {{input.key_messages}}

Divide the target audience into 3-5 actionable segments. For each:
1. **Name** — descriptive label
2. **Demographics** — role, company size, industry
3. **Pain points** — problems this product solves
4. **Motivations** — purchase decision drivers
5. **Messaging angle** — how to frame the value proposition
6. **Channel preference** — which platform(s) best reach this segment
