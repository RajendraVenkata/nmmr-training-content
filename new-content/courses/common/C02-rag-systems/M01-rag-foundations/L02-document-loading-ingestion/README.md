# L02: Document Loading & Ingestion

## Overview

This lesson covers the first stage of the RAG pipeline: loading and ingesting documents from diverse sources. You will learn how to handle multiple file formats, normalize document content, and build a robust ingestion pipeline using LlamaHub data loaders.

## Topics Covered

- Ingesting PDFs, markdown files, and HTML pages
- Using LlamaHub data loaders for standardized ingestion
- Document normalization and metadata extraction
- Handling encoding issues, special characters, and malformed documents
- Designing ingestion pipelines that scale to large document collections

## Lab: Building a Document Ingestion Pipeline for Multiple File Formats

Build an end-to-end ingestion pipeline that accepts PDFs, markdown files, and HTML pages, normalizes their content into a uniform document representation, and extracts relevant metadata for downstream processing.

### Lab Objectives

- Configure LlamaHub data loaders for PDF, markdown, and HTML sources
- Implement document normalization to produce clean, consistent text output
- Extract and attach metadata (source, title, date, file type) to each ingested document
- Handle common ingestion errors gracefully with logging and retry logic

## Key Takeaways

- A well-designed ingestion pipeline handles multiple file formats through a unified interface
- LlamaHub provides pre-built data loaders that simplify ingestion of common document types
- Document normalization ensures consistent downstream processing regardless of the original source format
- Metadata extraction during ingestion enables filtering and attribution in later retrieval stages
