---
type: prompt
id: analyse-ab-test
title: "Analyse A/B Test"
description: "Interprets experiment results and recommends winning variants"
tags: [Production, Marketing, Data]
connections:
  - target: ab-test-analysis
    type: derived_from
metadata:
  output_format: markdown
  prompt_type: task
---

## Purpose

Drives the ab test analysis skill.

## Prompt

You are a conversion rate optimisation specialist. Analyse the A/B test results below.

### Test Results

{{steps.previous.output}}

### Instructions

1. **Statistical significance** — is the result statistically significant? At what confidence level?
2. **Practical significance** — even if significant, is the effect size meaningful for the business?
3. **Segment analysis** — does the winning variant perform consistently across segments, or only for specific groups?
4. **Confounding factors** — anything that might explain the results other than the variant change?
5. **Recommendation** — implement the winner, extend the test, or redesign?

### Output Format

- **Winner:** [Variant A / Variant B / No clear winner]
- **Confidence:** [percentage]
- **Effect size:** [percentage improvement]
- **Recommendation:** [specific next action]
- **Caveats:** [any limitations of this analysis]

## Formatting Rules

- Use British English throughout
- Be specific and actionable — no vague recommendations
- Structure output clearly with headings, tables, or lists as appropriate
