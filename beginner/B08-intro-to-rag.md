# Module B8: Introduction to RAG (Retrieval Augmented Generation)

## Duration: 5-6 hours | Lab: Chat with PDF

## Learning Objectives
- Understand why RAG exists and the problem it solves
- Split documents into effective chunks for retrieval
- Create and use text embeddings for semantic search
- Set up ChromaDB as a local vector database
- Build a complete RAG pipeline with LangChain
- Evaluate RAG quality — Is the system retrieving the right information?

## Topics

### B8.1 The Problem — LLMs Don't Know Your Private Data
- LLMs are trained on public internet data with a knowledge cutoff
- They can't access your company docs, PDFs, databases, or internal wikis
- Hallucination risk increases when asked about unknown topics
- RAG: The solution — Give the LLM relevant context at query time

### B8.2 What is RAG — Retrieve → Augment → Generate
- **Retrieve**: Search a knowledge base for relevant documents
- **Augment**: Insert retrieved documents into the LLM prompt as context
- **Generate**: LLM answers the question using the provided context
- The RAG pipeline diagram
- RAG vs Fine-tuning — When to use which

### B8.3 Text Splitting and Chunking Strategies
- Why splitting matters — Documents are too large for context windows
- **Fixed-size chunking**: Split every N characters/tokens
- **Recursive character splitting**: Split on paragraphs → sentences → words
- **Chunk overlap**: Why overlapping chunks improve retrieval
- Chunk size tradeoffs: Too small = no context, too large = irrelevant noise
- LangChain text splitters

### B8.4 Embeddings — Converting Text to Vectors
- What embeddings are — Dense vector representations of meaning
- Similar text → Similar vectors (close in vector space)
- Embedding models: Sentence-Transformers (local, free), OpenAI Ada
- Generating embeddings with LangChain
- Embedding dimensions and their meaning

### B8.5 Vector Databases — ChromaDB (Local, Free)
- What vector databases do — Store and search embeddings efficiently
- ChromaDB: Simple, local, Python-native vector store
- Creating collections, adding documents, querying
- Similarity search — Finding the most relevant chunks
- Metadata filtering — Narrowing search by source, date, category

### B8.6 Building a Simple RAG Pipeline
- Step 1: Load documents (PDF, text, markdown)
- Step 2: Split into chunks
- Step 3: Generate embeddings
- Step 4: Store in ChromaDB
- Step 5: Query — Embed the question, search for similar chunks
- Step 6: Pass retrieved chunks + question to LLM
- Step 7: LLM generates answer grounded in the retrieved context

### B8.7 RAG with LangChain — Document Loaders, Retrievers, Chains
- Document loaders: `PyPDFLoader`, `TextLoader`, `WebBaseLoader`
- Retrievers: `ChromaDB.as_retriever()`
- RAG chain: `RetrievalQA` or LCEL-based retrieval chain
- Prompt template for RAG — "Answer based on the following context..."
- Returning source documents with answers

### B8.8 Lab: Build a "Chat with Your PDF" Application
- Load a PDF document
- Split, embed, and store in ChromaDB
- Build a RAG chain that answers questions from the PDF
- Add conversation memory for follow-up questions
- Compare answers with and without RAG

## Lab Exercises
1. Load a sample PDF and split it into chunks (experiment with chunk sizes)
2. Generate embeddings and store them in ChromaDB
3. Perform a similarity search — Query ChromaDB and see what comes back
4. Build a complete RAG chain with LangChain + Ollama
5. Ask questions and verify the answers cite the correct source passages
6. Compare: Ask the same question with RAG vs without RAG — Note the accuracy difference

## Key Takeaways
- RAG solves the "LLMs don't know your data" problem without fine-tuning
- Chunking strategy significantly impacts retrieval quality
- Embeddings capture semantic meaning — Similar questions find similar answers
- ChromaDB provides a free, local vector database perfect for development
- RAG + Agents is the most common production AI architecture

---
*Next: [Module B9 — Provider Abstraction: Write Once, Run Anywhere →](B09-provider-abstraction.md)*
