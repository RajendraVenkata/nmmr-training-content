# L01: BM25 Keyword Search

## Overview

This lesson introduces BM25, the foundational keyword-based retrieval algorithm used in search engines and RAG systems. You will learn how BM25 scores documents based on term frequency and inverse document frequency, and understand when keyword search remains the best choice.

## Topics Covered

- How BM25 works: the ranking function and its parameters
- Term Frequency (TF): measuring how often a term appears in a document
- Inverse Document Frequency (IDF): weighting rare terms higher than common ones
- Document length normalization in BM25
- When keyword search excels over semantic search (exact matches, technical terms, proper nouns)
- Limitations of keyword search: vocabulary mismatch and lack of semantic understanding

## Key Takeaways

- BM25 is a probabilistic ranking function that scores documents based on term overlap with the query
- IDF weighting ensures that distinctive terms contribute more to relevance than common words
- Keyword search excels when queries contain exact technical terms, product names, or identifiers
- BM25 struggles with synonyms, paraphrases, and queries that require semantic understanding
- Despite being decades old, BM25 remains a strong baseline and a valuable component of hybrid retrieval systems
