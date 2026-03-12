# L04: Deduplication & Corpus Quality

## Overview

Explore techniques for detecting and removing duplicate content from retrieval corpora and maintaining overall corpus quality over time. This lesson covers near-duplicate detection algorithms, quality scoring methodologies, and strategies for keeping retrieval corpora fresh and relevant.

## Topics Covered

- Near-duplicate detection using MinHash and SimHash
- Exact deduplication strategies and their limitations
- Corpus quality scoring frameworks
- Removing low-quality content (boilerplate, spam, outdated material)
- Maintaining corpus freshness with update and retirement policies
- Monitoring corpus health metrics over time

## Key Takeaways

- Duplicate content in retrieval corpora wastes storage, increases latency, and can bias retrieval results
- Near-duplicate detection is more important than exact deduplication in practice, as content is often reformatted or slightly modified
- Corpus quality scoring should consider multiple dimensions: relevance, accuracy, recency, and completeness
- A corpus is a living system that requires ongoing maintenance; automated quality monitoring prevents gradual degradation
- Freshness policies should balance adding new content with retiring outdated material to keep the corpus relevant
