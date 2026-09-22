# DocuMind AI – RAG-Based PDF Question Answering

A Generative AI application that allows users to ask questions about
information contained in a TCS PDF document.

The project uses Retrieval-Augmented Generation (RAG) to retrieve
relevant information from the uploaded document and generate
context-aware answers using an LLM.

---

## 📌 Project Overview

Large PDF documents can contain a significant amount of information,
making it difficult to manually search for specific answers.

This project provides a document question-answering system where a user
can provide a TCS PDF and ask questions related to its content.

Instead of sending the complete document directly to the language model,
the system:

1. Loads the PDF document.
2. Extracts the document content.
3. Splits the content into smaller chunks.
4. Converts the chunks into vector embeddings.
5. Stores the embeddings in a FAISS vector database.
6. Retrieves the most relevant chunks for a user question.
7. Passes the retrieved context to an LLM.
8. Generates an answer based on the retrieved document context.

---

## 🚀 Key Features

- PDF document processing
- Text extraction from documents
- Text chunking using LangChain text splitters
- Semantic embeddings using Sentence Transformers
- Vector similarity search using FAISS
- Retrieval-Augmented Generation (RAG)
- LLM-based answer generation
- Question answering based on document context
- Reduces the need for manually searching large PDF documents

---

## 🧠 RAG Workflow

```text
                TCS PDF
                   |
                   ↓
            Document Loader
                   |
                   ↓
             Text Extraction
                   |
                   ↓
             Text Splitter
                   |
                   ↓
        Document Text Chunks
                   |
                   ↓
       Sentence Transformer
             Embeddings
                   |
                   ↓
          FAISS Vector Store
                   |
                   ↓
             User Question
                   |
                   ↓
       Question Embedding
                   |
                   ↓
       Similarity Search
                   |
                   ↓
        Relevant PDF Context
                   |
                   ↓
            LangChain
                   |
                   ↓
              OpenAI LLM
                   |
                   ↓
           Generated Answer

## 🛠️ Technologies Used

### Programming Language

- Python

### Generative AI

- Large Language Models (LLMs)
- Retrieval-Augmented Generation (RAG)
- Prompt Engineering

### Frameworks & Libraries

- LangChain
- Hugging Face
- Sentence Transformers

### Vector Database

- FAISS

### Document Processing

- PDF Document Loading
- Text Splitting
- Document Chunking

### LLM

- OpenAI

## 🔍 How It Works

### 1. PDF Upload

The application accepts a PDF document provided by the user and
extracts its textual content.

### 2. Text Splitting

The extracted document content is divided into smaller chunks using
text splitters.

### 3. Embedding Generation

Sentence Transformers convert the document chunks into numerical
vector representations.

### 4. Vector Storage

The generated embeddings are stored in a FAISS vector database for
efficient similarity search.

### 5. Question Processing

The user asks a question related to the uploaded PDF.

### 6. Similarity Search

FAISS searches for document chunks that are semantically relevant
to the user's question.

### 7. Context Retrieval

The most relevant document chunks are retrieved and provided as
context to the language model.

### 8. Answer Generation

LangChain combines the retrieved context with the user's question
and sends it to the OpenAI LLM to generate a context-aware answer.

The system generates answers based on the information retrieved
from the uploaded PDF.

## 💬 Example Questions

Users can upload different PDF documents and ask questions such as:

- What is the main topic of this document?
- What are the key points discussed?
- Summarize the important information.
- What does the document say about [specific topic]?
- What are the important figures or facts mentioned?
- Explain [specific concept] from the document.

