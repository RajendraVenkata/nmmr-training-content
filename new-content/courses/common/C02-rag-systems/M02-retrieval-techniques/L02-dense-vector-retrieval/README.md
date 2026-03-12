# L02: Dense Vector Retrieval

## Overview

This lesson covers semantic search using dense vector embeddings, where queries and documents are compared based on meaning rather than exact word overlap. You will learn how similarity metrics work and why dense retrieval captures semantic relationships that keyword search misses.

## Topics Covered

- Semantic search with embeddings: matching by meaning instead of keywords
- Similarity metrics: cosine similarity, dot product, and Euclidean distance
- How bi-encoder models generate query and document embeddings independently
- Advantages over keyword search: handling synonyms, paraphrases, and conceptual queries
- Approximate Nearest Neighbor (ANN) search for scalable retrieval
- Limitations of dense retrieval: sensitivity to embedding model quality and out-of-domain queries

## Key Takeaways

- Dense vector retrieval encodes both queries and documents into the same embedding space, enabling semantic matching
- Cosine similarity is the most common metric for comparing embedding vectors, measuring the angle between them
- Dense retrieval handles synonyms and paraphrases naturally, unlike keyword-based approaches
- The quality of retrieval depends heavily on the embedding model and how well it represents your domain
- ANN algorithms (HNSW, IVF) make dense retrieval practical at scale by trading a small amount of accuracy for large speed gains
