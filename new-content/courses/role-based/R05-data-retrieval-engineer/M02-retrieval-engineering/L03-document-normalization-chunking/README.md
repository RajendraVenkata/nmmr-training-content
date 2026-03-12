# L03: Document Normalization & Chunking Policies

## Overview

Learn how to standardize diverse document formats and design chunking policies that balance retrieval granularity with context preservation. This lesson covers handling complex document elements like tables and images, preserving metadata through the pipeline, and building configurable chunking systems.

## Topics Covered

- Standardizing document formats across diverse sources
- Chunking policy design (size, overlap, semantic boundaries)
- Handling tables, images, and mixed-content documents
- Metadata preservation throughout the normalization pipeline
- Configurable chunking systems for different use cases
- Evaluating chunk quality and retrieval impact

## Lab: Building a Document Normalization and Chunking Pipeline

Build a configurable pipeline that normalizes documents from multiple formats into a standard representation and applies different chunking policies, with evaluation of how each policy affects retrieval quality.

### Lab Objectives

- Implement document normalization for at least three input formats (PDF, HTML, Markdown)
- Build a chunking engine with configurable size, overlap, and boundary detection
- Preserve document metadata (title, section headers, page numbers) through the pipeline
- Evaluate retrieval quality across different chunking configurations

## Key Takeaways

- Document normalization into a common intermediate format simplifies all downstream processing
- Chunk size and overlap are not one-size-fits-all; they should be tuned per corpus and use case
- Semantic boundary detection (respecting section, paragraph, and sentence boundaries) produces better chunks than fixed-size splitting
- Metadata preservation is essential for filtering, citation, and context reconstruction at retrieval time
