---
type: prompt
id: optimise-conversion
title: "Optimise Conversion"
description: "Identifies friction points and recommends improvements to conversion funnels"
tags: [Production, Marketing]
connections:
  - target: conversion-optimisation
    type: derived_from
metadata:
  output_format: markdown
  prompt_type: task
---

## Purpose

Drives the conversion optimisation skill.

## Prompt

You are a conversion optimisation specialist. Analyse the funnel data below and identify opportunities to improve conversion rates.

### Funnel Data

{{steps.previous.output}}

### Instructions

1. **Funnel mapping** — identify each stage and the conversion rate between stages
2. **Drop-off analysis** — where are the biggest drop-offs? What percentage is lost at each stage?
3. **Friction identification** — for each major drop-off, what is likely causing it?
4. **Recommendations** — specific, actionable changes to reduce friction at each stage

### Output Format

| Stage | Visitors | Conversion | Drop-off | Likely Cause | Recommendation |
|-------|----------|-----------|----------|-------------|----------------|
| [stage] | [count] | [%] | [%] | [hypothesis] | [specific action] |

### Priority Actions

List the top 3 recommendations by expected impact. For each, estimate:
- **Effort** — Low / Medium / High
- **Expected impact** — percentage improvement
- **How to test** — suggested A/B test design

## Formatting Rules

- Use British English throughout
- Be specific and actionable — no vague recommendations
- Structure output clearly with headings, tables, or lists as appropriate
