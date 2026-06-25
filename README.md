# Retrieval-Augmented-Generation Based-Q-A-System

# Company Policy RAG Chatbot

A Retrieval-Augmented Generation (RAG) chatbot that answers questions from company policy documents using semantic search and a local Large Language Model (LLM).

# Overview

This project enables users to ask natural language questions about company policies and receive accurate, context-aware answers. Instead of relying solely on an LLM's internal knowledge, the system retrieves relevant information from a document knowledge base and uses that context to generate responses.

# Features
Document-based question answering
Semantic search using vector embeddings
Persistent vector storage with ChromaDB
Local inference using TinyLlama
Retrieval-Augmented Generation (RAG) architecture
No dependency on external APIs for inference
# Tech Stack
Python
LangChain
ChromaDB
Hugging Face Transformers
Sentence Transformers (all-MiniLM-L6-v2)
TinyLlama-1.1B-Chat
# Architecture
Company Policy Documents
           │
           ▼
    Data Processing
           │
           ▼
      Embeddings
 (all-MiniLM-L6-v2)
           │
           ▼
       ChromaDB
    Vector Database
           │
           ▼
        Retriever
           │
           ▼
      TinyLlama LLM
           │
           ▼
     Generated Answer
# Workflow
Load company policy data from a JSONL dataset.
Convert records into LangChain documents.
Generate embeddings using Sentence Transformers.
Store embeddings in ChromaDB.
Retrieve the most relevant documents for a user query.
Pass retrieved context and query to TinyLlama.
Generate a context-based answer.
# Example

Question

Why is company policy reviewed every year?

Answer

Company policies are reviewed annually to ensure compliance with regulations, align with business objectives, and incorporate organizational changes.
# Key Learning Outcomes
Implemented an end-to-end RAG pipeline.
Worked with vector databases and semantic search.
Integrated open-source LLMs for document-based QA.
Improved answer relevance by grounding responses in retrieved context.
Gained hands-on experience with LangChain and Hugging Face ecosystems.
