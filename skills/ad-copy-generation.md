---
type: skill
id: ad-copy-generation
title: Ad Copy Generation
description: "Generating platform-specific ad copy variants from audience segments, key messages, and platform constraints"
tags: [Production, Writing, Audience]
connections:
  - target: llm-service
    type: runs_on
metadata:
  estimated_duration: "5 minutes"
  avg_tokens: 3000
  trigger: manual
---

## Ad Copy Generation

This skill turns audience segments and campaign messages into ready-to-run, platform-specific ad copy — the primary deliverable of the pipeline.

### Core Capability

Given the audience segment profiles, the key messages, and any platform constraints, this skill drafts distinct ad variants that each lead with a different persuasion angle and respect the character limits of the target channel.

### Method

1. **Segment targeting:** Read the segment profiles — demographics, psychographics, pain points, and preferred channels — and match each variant to the segment and channel it is written for.
2. **Angle spread:** Produce five variants that span benefit-led, problem-solution, social proof, urgency, and curiosity so downstream A/B testing has genuinely divergent creative to compare.
3. **Constraint fit:** Apply the supplied platform constraints so every headline and description stays within its channel's character limits, and include a clear call to action in each variant.

### Output Structure

Five ad copy variants per segment per platform, each labelled with its angle and channel, forming the copy that the testing, optimisation, and language-polish stages then operate on.
