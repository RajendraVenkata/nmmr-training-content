# L03: Memory Management (Episodic & Semantic)

## Overview

This lesson covers memory management strategies for conversational AI agents, focusing on episodic memory for tracking past interactions and semantic memory for retrieving long-term contextual knowledge. You will learn how to build memory hierarchies that balance context richness with cost efficiency.

## Topics Covered

- Episodic memory for tracking past interactions and conversation history
- Semantic memory for retrieving long-term context and knowledge
- Memory hierarchies and tiered storage strategies
- Cost management for context windows
- Memory summarization and compression techniques
- Memory retrieval strategies for relevance and recency

## Lab: Implementing Episodic and Semantic Memory for a Conversational Agent

Build a conversational agent that uses episodic memory to recall previous conversation turns and semantic memory to retrieve relevant long-term knowledge, demonstrating how memory hierarchies manage context window costs.

### Lab Objectives

- Implement episodic memory that stores and retrieves recent conversation history
- Build semantic memory using a vector store for long-term knowledge retrieval
- Create a memory hierarchy that prioritizes recent episodic context and supplements with semantic recall
- Implement memory summarization to compress older interactions without losing key information
- Measure and optimize token usage across different memory strategies

## Key Takeaways

- Episodic memory stores sequential interaction history, enabling agents to reference previous conversations and maintain continuity
- Semantic memory uses vector embeddings to store and retrieve knowledge based on meaning, independent of when it was learned
- Memory hierarchies combine fast short-term recall with deep long-term retrieval, similar to human memory systems
- Context window costs grow linearly with memory size, making summarization and selective loading essential for production agents
- Effective memory management is the difference between an agent that feels stateless and one that maintains meaningful long-term relationships with users
