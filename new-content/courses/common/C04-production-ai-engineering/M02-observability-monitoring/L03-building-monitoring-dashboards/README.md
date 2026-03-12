# L03: Building Monitoring Dashboards

## Overview

This lesson covers how to design and build monitoring dashboards tailored to AI systems. You will learn which metrics to surface, how to organize dashboards for different audiences (engineers, managers, on-call), how to set up alerting on quality degradation, and how to integrate user feedback signals like thumbs up/down into your monitoring stack.

## Topics Covered

- Dashboard design principles for AI systems
- Key metrics to display: latency, throughput, error rates, quality scores, cost
- Alerting on quality degradation and anomaly detection
- Integrating user feedback (thumbs up/down) into monitoring
- Organizing dashboards for different stakeholders

## Lab: Building a Monitoring Dashboard for an AI System Using Arize Phoenix

Build a comprehensive monitoring dashboard using Arize Phoenix that visualizes key production metrics for an AI system, including latency distributions, quality scores, cost trends, and user feedback signals.

### Lab Objectives

- Set up Arize Phoenix and connect it to an instrumented AI application
- Create dashboard panels for latency (P50/P95/P99), throughput, and error rates
- Add quality metric visualizations including response relevance and citation coverage
- Configure alerting rules that fire when quality metrics drop below defined thresholds
- Integrate a thumbs up/down feedback mechanism and visualize feedback trends over time

## Key Takeaways

- AI monitoring dashboards must go beyond traditional infrastructure metrics to include quality signals that capture whether the AI is producing useful, accurate responses
- User feedback (thumbs up/down) is a lagging but essential signal; it provides ground truth about response quality that automated metrics can only approximate
- Alerts should be configured on rate-of-change in addition to absolute thresholds, so that gradual quality degradation is caught before it becomes severe
- Different stakeholders need different views: engineers need detailed traces and error breakdowns, while leadership needs cost trends and quality summaries
