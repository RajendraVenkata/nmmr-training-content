# L02: Eval-Gated Deployments

## Overview

This lesson focuses on using evaluation results as deployment gates, ensuring that only AI systems meeting defined quality thresholds reach production. You will learn how to set quality thresholds, configure automatic build failures when quality drops, and detect regressions introduced by prompt or configuration changes before they affect users.

## Topics Covered

- Defining quality thresholds for AI deployment readiness
- Configuring automatic build failure when evaluation scores drop below baselines
- Detecting regressions caused by prompt changes
- Comparing current build quality against historical baselines
- Strategies for handling borderline cases and threshold tuning

## Key Takeaways

- Eval-gated deployments enforce a simple principle: if the AI is not performing well enough, it does not ship, regardless of whether the code changes are correct
- Quality thresholds should be set based on production baselines rather than arbitrary targets; measure current production quality first, then set the gate slightly below to catch meaningful regressions
- Prompt changes are the most common source of AI quality regressions and are often invisible in traditional code review; eval gates catch these regressions automatically
- Threshold tuning requires balancing sensitivity (catching real regressions) against false positives (blocking valid deployments due to natural variance in non-deterministic AI outputs)
- Eval-gated pipelines should report detailed comparison data (which test cases degraded, by how much, and on which metrics) so that developers can quickly understand and fix regressions rather than just seeing a pass/fail result
