# L04: Embedding Generation & Storage

## Overview

This lesson covers how to convert text chunks into vector embeddings and store them in a vector database for efficient similarity search. You will learn what embeddings represent, how to choose an embedding model, and how to set up ChromaDB as your vector store.

## Topics Covered

- What embeddings are and how they capture semantic meaning
- Popular embedding models (OpenAI text-embedding-ada-002, Sentence Transformers, Cohere Embed)
- Vector representations: dimensions, normalization, and similarity
- Storing embeddings in vector databases (ChromaDB, Pinecone, Weaviate)
- Collection management, metadata filtering, and persistence in ChromaDB
- Batch embedding generation for large document sets

## Lab: Generating Embeddings and Storing Them in ChromaDB

Generate embeddings for a set of document chunks using a sentence transformer model, store them in a ChromaDB collection with metadata, and perform basic similarity queries to verify retrieval quality.

### Lab Objectives

- Set up ChromaDB locally and create a persistent collection
- Generate embeddings from text chunks using a sentence transformer model
- Store embeddings with associated metadata (source document, chunk index, title)
- Execute similarity search queries and evaluate the relevance of returned results

## Key Takeaways

- Embeddings are dense vector representations that encode semantic meaning, enabling similarity-based retrieval
- The choice of embedding model affects both the quality of retrieval and the dimensionality of stored vectors
- ChromaDB provides a lightweight, developer-friendly vector database suitable for prototyping and small-to-medium workloads
- Storing metadata alongside embeddings enables filtering and attribution during retrieval
