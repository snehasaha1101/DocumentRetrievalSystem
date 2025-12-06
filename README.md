# DocumentRetrievalSystem
# Built an AI-Powered Document Retrieval System with Docling and Granite

This project implements an end-to-end **Retrieval-Augmented Generation (RAG)** pipeline using:

- **IBM Granite** models (LLM + embeddings)
- **Docling** for document parsing and chunking
- **Milvus (milvus-lite)** as a vector database
- **LangChain** for orchestration

The example use case answers questions about **UFC 310** and official **UFC rules** by combining web articles and a PDF rulebook.

---

## 🚀 What This Project Does

1. **Processes documents** from multiple sources (web pages + PDF) using Docling  
2. **Chunks and embeds text** using a Granite embeddings model  
3. **Stores embeddings** in a Milvus vector database  
4. **Retrieves relevant chunks** for a user query  
5. **Uses Granite LLM** to generate answers grounded in those retrieved chunks (RAG)

The notebook walks through everything in a single, reproducible pipeline.

---

## 🧰 Tech Stack

- **Language model:** `ibm-granite/granite-4.0-h-small` via Replicate
- **Embeddings:** `ibm-granite/granite-embedding-30m-english`
- **Document processing:** [Docling](https://github.com/DS4SD/docling)
- **Vector database:** Milvus (local `milvus-lite` via `langchain-milvus`)
- **Orchestration:** LangChain (classic/core/milvus/huggingface/replicate clients)
- **Environment:** Google Colab (Python 3.12)

---

## 📁 Repository Structure

```text
.
├── Granite_Docling_RAG.ipynb   # Main notebook with the complete RAG pipeline
└── README.md                   # Project description and usage guide
