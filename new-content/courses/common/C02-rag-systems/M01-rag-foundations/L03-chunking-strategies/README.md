# L03: Chunking Strategies

## Overview

This lesson explores how to split documents into chunks that balance completeness and retrievability. You will learn how chunk size, overlap, and splitting method directly impact RAG retrieval quality, and compare multiple strategies on real documents.

## Topics Covered

- Why chunking matters for retrieval quality
- Chunk size selection: the 500-800 token sweet spot and its trade-offs
- Overlap strategies: using 100-token overlap to prevent context loss at boundaries
- Recursive chunking: splitting by paragraphs, sentences, then characters
- Semantic chunking and structure-aware splitting
- How chunk size affects embedding quality and retrieval precision

## Lab: Implementing and Comparing Different Chunking Strategies on Real Documents

Take a set of real-world documents and apply multiple chunking strategies (fixed-size, recursive, and semantic). Compare the resulting chunks for completeness, coherence, and retrieval effectiveness.

### Lab Objectives

- Implement fixed-size chunking with configurable token count and overlap
- Implement recursive chunking that respects document structure (headings, paragraphs, sentences)
- Compare chunk quality across strategies using coherence and boundary-integrity checks
- Measure the impact of chunk size and overlap on downstream retrieval accuracy

## Key Takeaways

- Chunk size is a critical hyperparameter: too small loses context, too large dilutes relevance
- Overlap between chunks prevents information loss at chunk boundaries
- Recursive chunking preserves document structure better than naive fixed-size splitting
- The optimal chunking strategy depends on document type, query patterns, and embedding model capabilities
