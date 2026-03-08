---
type: document
id: ab-testing-protocol
title: A/B Testing Protocol
description: "Standard process for running marketing experiments"
tags: [Internal]
connections: []
---

# A/B Testing Protocol

## Before Testing
1. State your hypothesis: "If we change X, then Y will happen because Z"
2. Calculate required sample size (use 80% power, 95% confidence)
3. Define primary metric and guard-rail metrics
4. Set test duration (minimum 7 days for email, 14 for landing pages)

## During Testing
- Do not peek at results before the test period ends
- Do not change anything mid-test
- Monitor guard-rail metrics for unexpected harm

## After Testing
- Check statistical significance (p < 0.05)
- Calculate practical effect size
- Document findings in the test log
- Implement winner or plan follow-up test
