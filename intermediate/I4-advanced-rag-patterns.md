# Course I4: Advanced RAG Patterns

> **Go beyond basic RAG** — Master advanced chunking strategies, hybrid search, re-ranking, multi-query RAG, self-corrective retrieval, and evaluation techniques for production-quality retrieval.

### Goal: Build production-grade RAG systems with high retrieval accuracy and answer quality

---

## I4.1 Limitations of Naive RAG
- The basic RAG problem — Simple vector search often retrieves irrelevant chunks
- Semantic gap — Query embeddings don't always match document embeddings
- Chunk boundary issues — Important context split across chunks
- Single-query limitation — One query may not capture all aspects of a question
- No verification — Naive RAG trusts whatever is retrieved
- Ranking quality — Vector similarity ≠ actual relevance
- When naive RAG fails — Complex questions, ambiguous queries, multi-hop reasoning

## I4.2 Chunking Strategies — Semantic, Recursive, Parent-Child (Lab)
- Recursive character splitting revisited — Optimizing chunk size and overlap
- Semantic chunking — Using embeddings to detect topic boundaries
- Parent-child chunking — Small chunks for retrieval, large chunks for context
- Document-aware chunking — Respecting headers, sections, and paragraphs
- Agentic chunking — Using an LLM to decide optimal chunk boundaries
- Multi-level indexing — Summary-level and detail-level chunks
- Chunk metadata enrichment — Adding titles, keywords, summaries to each chunk
- Evaluation — Measuring chunk quality and its impact on retrieval

## I4.3 Hybrid Search — Combining Vector Search + Keyword Search (BM25) (Lab)
- Vector search limitations — Misses exact keyword matches, struggles with names/codes
- BM25 keyword search — Traditional text search that excels at exact matching
- Why hybrid — Combine semantic understanding with keyword precision
- Reciprocal Rank Fusion (RRF) — Merging results from multiple search methods
- Weighted hybrid search — Tuning the balance between vector and keyword results
- Implementation with ChromaDB — Using ChromaDB's built-in hybrid capabilities
- Implementation with Elasticsearch — BM25 + dense vector in one index
- When hybrid shines — Technical docs, product catalogs, mixed query types

## I4.4 Re-Ranking — Cross-Encoder Models for Better Relevance (Lab)
- The re-ranking concept — Retrieve many, re-rank to find the best
- Bi-encoder vs cross-encoder — Why cross-encoders are more accurate but slower
- Cohere Rerank — Using Cohere's reranking API
- Local re-rankers — Cross-encoder models from Sentence Transformers
- ColBERT — Late interaction for efficient re-ranking
- The retrieve-then-rerank pipeline — Retrieve top-50, re-rank to top-5
- Evaluating re-ranker impact — Before and after retrieval quality metrics
- Cost-performance trade-off — When re-ranking is worth the extra latency

## I4.5 Multi-Query RAG — Generating Multiple Search Queries (Lab)
- The single-query problem — One query can't capture all angles of a complex question
- Query expansion — LLM generates 3-5 alternative queries for the same question
- Query decomposition — Breaking a complex question into simpler sub-questions
- HyDE (Hypothetical Document Embeddings) — Generate a hypothetical answer, use it to search
- Step-back prompting — Asking a more general question first
- Fusing results — Combining and deduplicating results from multiple queries
- Implementation with LangChain — `MultiQueryRetriever` for automatic query expansion

## I4.6 Self-Corrective RAG — Agent Verifies and Retries Retrieval
- The problem — Retrieved context may be irrelevant or insufficient
- Relevance checking — LLM evaluates whether retrieved docs answer the question
- Hallucination detection — Checking if the answer is grounded in retrieved context
- Retry with reformulated query — If retrieval fails, try a different query
- CRAG (Corrective RAG) — Retrieve → Grade → Rewrite → Retrieve again
- Knowledge refinement — Extracting only relevant sentences from retrieved chunks
- Web search fallback — If local retrieval fails, fall back to web search
- Implementation with LangGraph — Self-corrective RAG as a graph workflow

## I4.7 RAG Evaluation — Measuring Retrieval Quality and Answer Quality
- Why evaluation matters — You can't improve what you can't measure
- Retrieval metrics — Precision@K, Recall@K, MRR, NDCG
- Answer quality metrics — Faithfulness, relevance, completeness
- RAGAS framework — Automated RAG evaluation with LLM-as-judge
- Building evaluation datasets — Creating question-answer-context test sets
- Human evaluation — When and how to involve human raters
- Continuous evaluation — Monitoring RAG quality in production
- A/B testing — Comparing different RAG configurations
