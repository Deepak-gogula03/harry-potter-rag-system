# 📚 Harry Potter Knowledge Assistant using OpenAI, Pinecone & Retrieval-Augmented Generation (RAG)

🚀 Overview

This project implements an end-to-end Retrieval-Augmented Generation (RAG) pipeline capable of answering natural language questions from a large-scale document collection.

The system processes the complete Harry Potter book series, generates vector embeddings using OpenAI's embedding models, stores them in Pinecone Vector Database, retrieves relevant contextual information through semantic search, and generates accurate responses using GPT-4o Mini.

Unlike traditional keyword-based search systems, this solution leverages semantic understanding to retrieve relevant information and provide context-aware answers grounded in the source documents.

---

🎯 Project Objective

Large Language Models possess strong reasoning capabilities but lack access to custom knowledge sources unless explicitly provided with contextual information.

The objective of this project is to build a scalable document intelligence system that combines vector search and generative AI to answer questions directly from a custom knowledge base.

This implementation demonstrates how Retrieval-Augmented Generation can be used to improve response quality, reduce hallucinations, and enable knowledge retrieval from large document collections.

---

💼 Business Impact

Organizations generate and store large volumes of unstructured information, making knowledge retrieval difficult and time-consuming.

This project demonstrates how Retrieval-Augmented Generation (RAG) can transform static document repositories into intelligent knowledge systems capable of providing instant, context-aware answers.

Potential Real-World Applications
🏢 Enterprise Knowledge Bases.
📚 Internal Documentation Search.
🎧 Customer Support Assistants.
⚖️ Legal Document Analysis.
📑 Research Paper Assistants.
🎓 Educational Knowledge Platforms.
🏥 Healthcare & Financial Document Search Systems.

---

📖 Dataset Information

The knowledge base consists of the complete Harry Potter book collection.

📊 Dataset Statistics

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

📈 Project Metrics

| Metric                | Value                  |
| --------------------- | ---------------------- |
| Total Books Processed | 7                      |
| Total Pages Indexed   | 3,623                  |
| Total Vector Records  | 3,623                  |
| Embedding Dimension   | 1,536                  |
| Embedding Model       | text-embedding-3-small |
| Language Model        | GPT-4o Mini            |
| Vector Database       | Pinecone               |
| Similarity Metric     | Cosine Similarity      |
| Cloud Region          | AWS us-east-1          |

---

🏗️ System Architecture

<img width="1536" height="1024" alt="Architecture" src="https://github.com/user-attachments/assets/6be9647f-5430-4916-8dec-7ed917a5e885" />


The architecture follows a standard Retrieval-Augmented Generation workflow consisting of document processing, embedding generation, vector storage, similarity search, context retrieval, and answer generation.

---

✨ Key Features

📄 Document Processing

* Processes large-scale PDF collections
* Extracts and prepares textual content
* Enables document-level knowledge retrieval

✂️ Intelligent Text Chunking

* Splits large documents into optimized chunks
* Preserves contextual information
* Improves retrieval accuracy

🧠 OpenAI Embeddings

* Generates semantic vector representations
* Uses OpenAI's text-embedding-3-small model
* Produces 1,536-dimensional embeddings

🗄️ Pinecone Vector Database

* Stores document embeddings efficiently
* Supports scalable similarity search
* Enables high-performance retrieval

🔍 Semantic Search

* Retrieves information based on contextual meaning
* Eliminates dependence on exact keyword matching
* Improves relevance of retrieved content

💬 Context-Aware Question Answering

* Uses GPT-4o Mini for answer generation
* Generates grounded responses from retrieved context
* Improves factual accuracy and reduces hallucinations

---

🛠️ Technology Stack

| Component               | Technology                    |
| ----------------------- | ----------------------------- |
| Programming Language    | Python                        |
| Framework               | LangChain                     |
| Embedding Model         | OpenAI text-embedding-3-small |
| Language Model          | GPT-4o Mini                   |
| Vector Database         | Pinecone                      |
| Document Processing     | PyPDF                         |
| Development Environment | Jupyter Notebook              |

---

⚙️ Retrieval-Augmented Generation Workflow

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

📊 Pinecone Vector Database Metrics

The project successfully indexed the complete knowledge base into Pinecone.

📈 Vector Database Statistics

* Total Indexed Records: 3,623
* Vector Type: Dense
* Similarity Metric: Cosine Similarity
* Embedding Dimensions: 1,536
* Deployment Region: AWS us-east-1

---

❓ Sample Questions

* Who is Harry Potter?
* What are Horcruxes?
* Explain the significance of the Elder Wand.
* What happened during the Battle of Hogwarts?
* Describe the relationship between Harry Potter and Severus Snape.
* Who created the Marauder's Map?
* Explain the role of Albus Dumbledore throughout the series.

---

📥 Installation

Clone the repository:

```bash
git clone https://github.com/Deepak-gogula03/harry-potter-rag-system.git
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

🔐 Environment Configuration

Create a `.env` file in the project root directory:

```env
OPENAI_API_KEY=YOUR_OPENAI_API_KEY
PINECONE_API_KEY=YOUR_PINECONE_API_KEY
```

---

📁 Project Structure

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
│   ├── pinecone_index_overview.png
│   ├── vector_statistics.png
│   └── query_result.png
│
├── requirements.txt
├── README.md
└── .env.example
```

---

🌟 Project Highlights

* Built an end-to-end Retrieval-Augmented Generation (RAG) pipeline
* Indexed 3,623 pages of knowledge into Pinecone
* Generated 1,536-dimensional OpenAI embeddings
* Implemented semantic similarity search
* Integrated GPT-4o Mini for context-aware answer generation
* Demonstrated scalable document intelligence architecture

---

🧩 Technical Challenges Addressed

### Processing Large Document Collections

Processed and indexed a knowledge base consisting of 3,623 pages while maintaining retrieval efficiency and response quality.

### Semantic Information Retrieval

Implemented vector-based similarity search capable of retrieving contextually relevant information beyond traditional keyword matching.

### Context Preservation

Applied chunking strategies that preserve semantic meaning while optimizing embedding generation and retrieval performance.

### Scalable Vector Search

Leveraged Pinecone Vector Database to efficiently manage and retrieve thousands of indexed records.

### Grounded Answer Generation

Integrated retrieved context with GPT-4o Mini to improve factual accuracy and minimize hallucinated responses.

---
