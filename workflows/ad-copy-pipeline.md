---
type: workflow
id: ad-copy-pipeline
title: Ad Copy Pipeline
description: "Audience targeting, copy generation, variant testing, and optimisation"
tags: [Draft]
connections:
  - target: audience-segmentation
    type: uses
  - target: ad-copy-generator
    type: uses
  - target: ab-test-analysis
    type: uses
  - target: conversion-optimisation
    type: uses
metadata:
  estimated_duration: "10-20 minutes"
  trigger: manual
---

## Overview

This workflow produces platform-specific ad copy from audience research through to performance optimisation. It combines segmentation, creative generation, and data-driven testing to maximise ad effectiveness.

## Pipeline Stages

### Stage 1: Audience Segmentation

**Input:** Customer data, survey results, behavioural analytics

Invoke the **audience-segmentation** skill to identify distinct audience segments with shared characteristics and messaging angles.

**Output:** Segment profiles with demographics, psychographics, and preferred channels.

### Stage 2: Ad Copy Generation

**Input:** Audience segments, brand voice guidelines, key messages, platform constraints

Invoke the **ad-copy-generator** prompt to create platform-specific ad variants. Each variant uses a different persuasion angle: benefit-led, problem-solution, social proof, urgency, or curiosity.

**Output:** 5 ad copy variants per segment per platform.

### Stage 3: A/B Test Analysis

**Input:** Test results from running ad variants (conversions, sample sizes, confidence intervals)

Invoke the **ab-test-analysis** skill to determine statistical significance, identify the winning variant, and recommend next tests.

**Gate:** Tests must reach minimum sample size before analysis.

**Output:** Winner recommendation with effect size and follow-up suggestions.

### Stage 4: Conversion Optimisation

**Input:** Funnel data, landing page analytics, current conversion rates

Invoke the **conversion-optimisation** skill to identify drop-off points in the post-click journey and recommend improvements.

**Output:** Prioritised optimisation recommendations with expected impact.

## Error Handling

- If no segment shows clear differentiation, gather more behavioural data before proceeding
- If ad variants perform similarly, test more divergent creative angles rather than minor copy tweaks
- If conversion optimisation reveals landing page issues, address those before scaling ad spend
