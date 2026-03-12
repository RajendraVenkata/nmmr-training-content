# Automated Regression Gating in CI/CD

## Overview

Wire evaluation scripts into CI/CD pipelines so that any code or prompt change that drops quality below a defined threshold automatically fails the build, preventing regressions from reaching production.

## Topics Covered

- Integrating eval scripts into CI/CD pipelines
- Setting quality thresholds for merge gates
- Preventing quality regressions on code/prompt changes
- Automated build failure on quality drops

## Lab: Setting Up Eval-Gated CI/CD

Build a CI/CD pipeline that automatically runs evaluation scripts and blocks merges when quality metrics drop below defined thresholds.

### Lab Objectives

- Integrate evaluation scripts into a CI/CD pipeline
- Configure quality thresholds that must be met for builds to pass
- Test with a prompt change that causes a quality regression
- Verify the pipeline blocks the regression automatically

## Key Takeaways

- Eval-gated CI/CD prevents quality regressions from reaching production
- Every change (code or prompt) should be evaluated before deployment
- Automated gates are more reliable than manual review for quality assurance
