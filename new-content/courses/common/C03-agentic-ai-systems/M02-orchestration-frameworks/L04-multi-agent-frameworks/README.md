# L04: Multi-Agent Frameworks (CrewAI, AutoGen)

## Overview

This lesson explores multi-agent frameworks that coordinate groups of specialized AI agents to tackle complex tasks. You will learn how CrewAI organizes agents with defined roles and delegation, how AutoGen enables conversation-based agent coordination, and how Swarms provide alternative orchestration patterns.

## Topics Covered

- Coordinating specialized agent groups for complex tasks
- Manager-worker delegation patterns
- CrewAI roles, tasks, and crew orchestration
- AutoGen conversation patterns and agent coordination
- Swarms and alternative multi-agent orchestration approaches
- Choosing the right multi-agent framework for your use case

## Lab: Orchestrating a Multi-Agent System with CrewAI

Build a multi-agent system using CrewAI where specialized agents with distinct roles collaborate to complete a complex task through manager-worker delegation and structured task handoff.

### Lab Objectives

- Define specialized agent roles with distinct backstories, goals, and tool access
- Create tasks with clear descriptions, expected outputs, and agent assignments
- Configure a crew with sequential and hierarchical process types
- Implement manager-worker delegation where a manager agent decomposes work and assigns it to specialists
- Observe and trace inter-agent communication and task completion flow

## Key Takeaways

- Multi-agent systems decompose complex problems by assigning specialized roles to different agents, each with focused expertise
- CrewAI uses a role-based model where agents have defined backstories, goals, and tool access that shape their behavior
- AutoGen uses conversation patterns where agents collaborate through structured message exchanges
- Manager-worker delegation enables hierarchical task decomposition where a coordinator assigns sub-tasks to specialist agents
- Multi-agent systems introduce coordination overhead and should only be used when the task genuinely benefits from specialization
