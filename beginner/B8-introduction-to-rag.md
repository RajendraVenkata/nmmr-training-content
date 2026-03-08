# Course B8: Introduction to RAG (Retrieval Augmented Generation)

> **Give LLMs access to your private data** — Learn the RAG pipeline from scratch: text splitting, embeddings, vector databases, and building a complete "Chat with your documents" application.

### Goal: Build a working RAG pipeline that lets users chat with their own documents

---

## B8.1 The Problem — LLMs Don't Know Your Private Data
- The knowledge cutoff — Models are trained on data up to a certain date
- No access to private data — LLMs can't read your company docs, databases, or files
- Hallucination risk — Without real data, models make up answers
- Fine-tuning is expensive — Training a model on your data is costly and time-consuming
- The RAG alternative — Feed relevant context at query time without retraining
- When to use RAG — Private data, frequently updated data, domain-specific knowledge

## B8.2 What is RAG — Retrieve → Augment → Generate
- The RAG pipeline — Three steps: retrieve relevant documents, augment the prompt, generate an answer
- Step 1: Retrieve — Search a knowledge base for documents relevant to the user's question
- Step 2: Augment — Insert retrieved documents into the LLM's prompt as context
- Step 3: Generate — The LLM generates an answer grounded in the retrieved context
- RAG vs fine-tuning — RAG is dynamic and cheap, fine-tuning is static and expensive
- RAG advantages — No retraining, always up-to-date, traceable sources, lower cost
- The RAG architecture diagram — Ingestion pipeline → Vector store ← Query pipeline

## B8.3 Text Splitting and Chunking Strategies (Lab)
- Why chunking matters — Documents must be split into smaller pieces for embedding and retrieval
- Naive splitting — Fixed character count, why it's problematic (splits mid-sentence)
- Recursive character splitting — `RecursiveCharacterTextSplitter` with separators hierarchy
- Chunk size — Choosing optimal size (500-1000 tokens), impact on retrieval quality
- Chunk overlap — Overlapping chunks to preserve context across boundaries (50-200 tokens)
- Sentence-based splitting — Splitting on sentence boundaries for cleaner chunks
- Markdown/HTML-aware splitting — Respecting document structure (headers, sections)
- Semantic chunking — Splitting based on topic changes using embeddings
- Metadata preservation — Keeping source, page number, section title with each chunk

## B8.4 Embeddings — Converting Text to Vectors (Lab)
- What are embeddings — Dense vector representations of text meaning
- How embeddings work — Mapping text to points in high-dimensional space
- Semantic similarity — Similar meanings = nearby vectors
- Embedding models — Sentence Transformers, OpenAI `text-embedding`, Nomic Embed, Cohere Embed
- Local embeddings with Ollama — Using `nomic-embed-text` or `all-minilm` for free local embeddings
- Embedding dimensions — 384, 768, 1024, 1536 — quality vs storage trade-offs
- Cosine similarity — Measuring distance between embedding vectors
- Embedding entire chunks — Processing your document chunks into vectors
- Batch embedding — Efficiently embedding large document collections

## B8.5 Vector Databases — ChromaDB (Local, Free) (Lab)
- What is a vector database — A database optimized for storing and searching embeddings
- Why you need one — Fast similarity search across millions of vectors
- ChromaDB — Lightweight, local, Python-native vector database
- Installing ChromaDB — `pip install chromadb`
- Creating a collection — `chroma_client.create_collection()`
- Adding documents — Storing text chunks with embeddings and metadata
- Querying — Similarity search with `collection.query()`
- Filtering — Metadata filters to narrow search scope
- Persistence — Saving and loading ChromaDB to/from disk
- Alternatives overview — Pinecone (cloud), Weaviate (hybrid), Qdrant (performance), FAISS (lightweight)

## B8.6 Building a Simple RAG Pipeline (Lab)
- The complete flow — Load → Split → Embed → Store → Query → Retrieve → Augment → Generate
- Loading documents — Reading PDF, text, markdown files
- Processing pipeline — Splitting and embedding documents
- Storing in ChromaDB — Building the vector index
- Query pipeline — User question → embed → search → retrieve top-k chunks
- Prompt construction — Inserting retrieved chunks into the LLM prompt
- Generating answers — LLM responds using the provided context
- Source attribution — Showing which documents the answer came from
- End-to-end code — Complete working RAG pipeline in Python

## B8.7 RAG with LangChain — Document Loaders, Retrievers, Chains
- LangChain's RAG abstractions — Simplified pipeline with pre-built components
- Document loaders — `PyPDFLoader`, `TextLoader`, `DirectoryLoader`, `WebBaseLoader`
- Text splitters — `RecursiveCharacterTextSplitter` integrated with LangChain
- Embeddings — `OllamaEmbeddings`, `OpenAIEmbeddings`, `HuggingFaceEmbeddings`
- Vector stores — `Chroma`, `FAISS` — LangChain wrappers for vector databases
- Retrievers — `vectorstore.as_retriever()` with `search_kwargs`
- RAG chain — `create_retrieval_chain()` or LCEL `retriever | prompt | model | parser`
- Stuff vs Map-Reduce — Strategies for handling many retrieved documents
- Conversational RAG — Adding memory to RAG for follow-up questions
