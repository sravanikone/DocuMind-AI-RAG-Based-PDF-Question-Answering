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
