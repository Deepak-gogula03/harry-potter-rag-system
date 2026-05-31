# 📚 Harry Potter Knowledge Assistant using OpenAI, Pinecone & Retrieval-Augmented Generation (RAG)

## Overview

This project implements an end-to-end Retrieval-Augmented Generation (RAG) pipeline capable of answering natural language questions from a large-scale document collection.

The system processes the complete Harry Potter book series, generates vector embeddings using OpenAI's embedding models, stores them in Pinecone Vector Database, retrieves relevant contextual information through semantic search, and generates accurate responses using GPT-4o Mini.

Unlike traditional keyword-based search systems, this solution leverages semantic understanding to retrieve relevant information and provide context-aware answers grounded in the source documents.

---

## Project Objective

Large Language Models possess strong reasoning capabilities but lack access to custom knowledge sources unless explicitly provided with contextual information.

The objective of this project is to build a scalable document intelligence system that combines vector search and generative AI to answer questions directly from a custom knowledge base.

This implementation demonstrates how Retrieval-Augmented Generation can be used to improve response quality, reduce hallucinations, and enable knowledge retrieval from large document collections.

---

## Dataset Information

The knowledge base consists of the complete Harry Potter book collection.

### Dataset Statistics

| Metric          | Value                   |
| --------------- | ----------------------- |
| Source          | Harry Potter Collection |
| Number of Books | 7                       |
| Total Pages     | 3,623                   |
| Vector Database | Pinecone                |
| Embedding Model | text-embedding-3-small  |
| Language Model  | GPT-4o Mini             |
| Indexed Records | 3,623                   |

The documents are processed, chunked, converted into embeddings, and stored in Pinecone to enable semantic retrieval.

---

## System Architecture

<img width="1536" height="1024" alt="Architecture" src="https://github.com/user-attachments/assets/dc54ad59-ae7b-45e3-8537-54e1943f9597" />


The architecture follows a standard Retrieval-Augmented Generation workflow consisting of document processing, embedding generation, vector storage, similarity search, context retrieval, and answer generation.

---

## Key Features

### Document Processing

* Loads and processes large PDF documents
* Extracts textual content from multiple documents
* Prepares documents for vectorization

### Text Chunking

* Splits large documents into manageable chunks
* Preserves contextual information
* Improves retrieval quality

### OpenAI Embeddings

* Generates dense vector representations
* Uses OpenAI's `text-embedding-3-small`
* Produces 1536-dimensional embeddings

### Pinecone Vector Database

* Stores document embeddings efficiently
* Enables high-performance similarity search
* Supports scalable vector retrieval

### Semantic Search

* Retrieves relevant information based on meaning
* Eliminates dependence on exact keyword matching
* Improves contextual relevance

### Context-Aware Question Answering

* Uses GPT-4o Mini for answer generation
* Generates responses using retrieved context
* Produces grounded and relevant answers

---

## Technology Stack

| Component               | Technology             |
| ----------------------- | ---------------------- |
| Programming Language    | Python                 |
| Framework               | LangChain              |
| Embedding Model         | text-embedding-3-small |
| Language Model          | GPT-4o Mini            |
| Vector Database         | Pinecone               |
| Document Processing     | PyPDF                  |
| Development Environment | Jupyter Notebook       |

---

## Retrieval-Augmented Generation Workflow

### Step 1: Document Loading

The Harry Potter book collection is loaded and processed using document loaders.

### Step 2: Text Chunking

The extracted content is divided into smaller chunks to improve retrieval efficiency and contextual relevance.

### Step 3: Embedding Generation

Each chunk is converted into vector embeddings using OpenAI's embedding model.

### Step 4: Vector Storage

Generated embeddings are stored inside Pinecone Vector Database.

### Step 5: Similarity Search

When a user submits a query, the query is converted into an embedding and compared against stored vectors.

### Step 6: Context Retrieval

The most relevant chunks are retrieved from Pinecone based on semantic similarity.

### Step 7: Response Generation

Retrieved context is supplied to GPT-4o Mini, which generates a context-aware response.

---

## Pinecone Vector Database Metrics

The project successfully indexed the complete knowledge base into Pinecone.

### Vector Database Statistics

* Total Indexed Records: 3,623
* Vector Type: Dense
* Similarity Metric: Cosine Similarity
* Embedding Dimensions: 1,536
* Deployment Region: AWS us-east-1

---

## Sample Questions

The system can answer questions such as:

* Who is Harry Potter?
* What are Horcruxes?
* Explain the significance of the Elder Wand.
* What happened during the Battle of Hogwarts?
* Describe the relationship between Harry Potter and Severus Snape.
* Who created the Marauder's Map?
* Explain the role of Albus Dumbledore throughout the series.

---

## Installation

Clone the repository:

```bash
git clone https://github.com/yourusername/harry-potter-rag-system.git
```

Move into the project directory:

```bash
cd harry-potter-rag-system
```

Install the required dependencies:

```bash
pip install -r requirements.txt
```

---

## Environment Configuration

Create a `.env` file in the project root directory:

```env
OPENAI_API_KEY=YOUR_OPENAI_API_KEY
PINECONE_API_KEY=YOUR_PINECONE_API_KEY
```

---

## Project Structure

```text
harry-potter-rag-system/
│
├── notebooks/
│   └── harry_potter_rag_system.ipynb
│
├── documents/
│   └── HarryPotterBooks.pdf
│
├── screenshots/
│   ├── architecture.png
│   ├── pinecone_index_overview.png
│   ├── vector_statistics.png
│   └── query_result.png
│
├── requirements.txt
├── README.md
├── .gitignore
└── .env.example
```

---

## Project Highlights

* Built an end-to-end Retrieval-Augmented Generation pipeline
* Indexed 3,623 pages of knowledge into Pinecone
* Generated 1,536-dimensional OpenAI embeddings
* Implemented semantic similarity search
* Integrated GPT-4o Mini for context-aware answer generation
* Demonstrated scalable document intelligence architecture

---


