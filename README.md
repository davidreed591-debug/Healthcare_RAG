# Healthcare Retrieval-Augmented Generation (RAG) System

A healthcare-focused Retrieval-Augmented Generation (RAG) application that combines vector search and Large Language Models (LLMs) to generate source-grounded responses from the Merck Manuals medical reference library.

## Overview

This project demonstrates the development of a Retrieval-Augmented Generation (RAG) application designed to assist healthcare professionals in accessing reliable medical knowledge from large clinical reference manuals.

The system combines Large Language Models (LLMs) with vector-based document retrieval to answer medical questions using information sourced from the Merck Manuals, a trusted medical reference containing thousands of pages of clinical content.

The goal of this project was to explore how RAG architectures can reduce hallucinations, improve response accuracy, and provide source-grounded answers in high-information environments such as healthcare.

### Technical Skills Demonstrated
- Retrieval-Augmented Generation (RAG)
- Large Language Model (LLM) Integration
- Prompt Engineering
- Vector Databases
- Semantic Search
- Information Retrieval
- Natural Language Processing (NLP)
- AI Application Development
- Python Programming
- Git Version Control

## Business Problem

Healthcare professionals often need to make time-sensitive decisions while navigating large volumes of medical literature and clinical guidelines.

Traditional LLMs can provide useful responses but may:

Generate unsupported information (hallucinations)
Lack access to domain-specific knowledge
Struggle with large reference documents
Provide answers without traceable sources

This project addresses these challenges by creating a system that retrieves relevant medical content before generating a response, ensuring answers are grounded in trusted documentation.

## Solution

The application processes a large medical reference corpus and transforms it into a searchable knowledge base using vector embeddings and semantic retrieval.

When a user submits a medical question:

- The query is converted into a vector embedding.
- The system searches a vector database for the most relevant medical passages.
- Retrieved context is injected into the LLM prompt.
- The model generates a response grounded in source material.
- Supporting references are returned alongside the answer.

This approach significantly improves reliability compared to using an LLM without retrieval.

## Results
Built an end-to-end RAG pipeline capable of searching thousands of pages of medical documentation.
Implemented semantic retrieval using vector embeddings and similarity search.
Reduced the likelihood of hallucinated responses by grounding answers in trusted medical references.
Demonstrated how enterprise knowledge bases can be integrated with modern LLM workflows.
Created a reusable framework that can be adapted to legal, financial, technical documentation, and customer support use cases.

Solution Architecture:
1. Document Processing
- Loaded the Merck Manuals reference library
- Extracted and cleaned document text
- Prepared content for retrieval and indexing
2. Text Chunking
- Split documents into overlapping text chunks
- Preserved contextual information across chunk boundaries
- Optimized chunk sizes for embedding generation
3. Embedding Generation
- Converted document chunks into vector embeddings using OpenAI Embeddings
- Created semantic representations of medical content
4. Vector Database
- Stored embeddings in a Chroma vector database
- Persisted vectors for efficient retrieval
5. Retrieval Layer
- Performed similarity searches against the vector store
- Retrieved the most relevant passages for a given query
6. Response Generation
- Injected retrieved context into an LLM prompt
- Generated source-grounded answers
- Included supporting references
7. Evaluation
- Compared baseline LLM responses with RAG-enhanced responses
- Assessed groundedness, relevance, and context utilization
  
### Example Questions

The system was tested on healthcare-related questions such as:

- What is the protocol for managing sepsis in a critical care unit?
- What are the symptoms and treatment options for appendicitis?
- What causes patchy hair loss and how is it treated?
- What interventions are recommended following traumatic brain injury?
  
## Technologies Used
- Programming Language : Python
- Artificial Intelligence & Machine Learning
- OpenAI GPT-4.1
- OpenAI Embeddings
- Retrieval-Augmented Generation (RAG)
- Semantic Search
- Vector Embeddings
- Frameworks & Libraries
- LangChain
- ChromaDB
- PyMuPDF
- Tiktoken
- Pandas
- NumPy
- Data Storage & Retrieval
- Chroma Vector Database
- Document Chunking
- Similarity Search
- Vector Indexing
- Development Environment
- Google Colab
- Jupyter Notebook
- Git
- GitHub
  
## Data Sources
Merck Manuals Medical Reference Library
