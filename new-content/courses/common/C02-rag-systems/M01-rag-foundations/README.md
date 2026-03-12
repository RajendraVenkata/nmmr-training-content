# M01: RAG Foundations

## Overview

This module introduces the core architecture and building blocks of Retrieval-Augmented Generation systems. You will learn how to load documents from diverse sources, split them into effective chunks, generate vector embeddings, and store them in a vector database for retrieval.

## Prerequisites

- Python programming proficiency
- Basic understanding of LLMs and how they generate text
- Familiarity with file formats (PDF, HTML, Markdown)
- Command-line comfort for installing packages and running scripts

## Lessons

| Lesson | Name | Has Lab? | Key Topics |
|--------|------|----------|------------|
| L01 | RAG Architecture Overview | No | What is RAG, why RAG over fine-tuning, the 5 stages, enterprise use cases |
| L02 | Document Loading & Ingestion | Yes | Ingesting PDFs, markdown, HTML; LlamaHub data loaders; document normalization |
| L03 | Chunking Strategies | Yes | Chunk size selection, overlap strategies, preventing context loss, recursive chunking |
| L04 | Embedding Generation & Storage | Yes | What embeddings are, embedding models, vector representations, vector database storage |

## Key Tools

- LlamaIndex and LlamaHub data loaders
- Python file handling libraries (PyPDF2, BeautifulSoup, markdown parsers)
- Sentence Transformers (embedding models)
- ChromaDB (vector database)

## Learning Outcomes

- Describe the end-to-end RAG pipeline and explain each of its five stages
- Justify when to use RAG versus fine-tuning for knowledge-grounded applications
- Build a document ingestion pipeline that handles PDFs, markdown, and HTML sources
- Apply chunking strategies with appropriate size and overlap parameters to preserve context
- Generate embeddings from text chunks and store them in ChromaDB for efficient retrieval
