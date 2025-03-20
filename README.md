# 🚀 AI-Powered Research Paper Q&A with RAG, Groq & Mixtral
### 🔍 Overview
This project implements a Retrieval-Augmented Generation (RAG) pipeline using FAISS, Hugging Face embeddings, and Groq’s Mixtral-8x7B to enable efficient, context-aware question-answering on research papers. It provides an interactive Streamlit UI for querying PDFs and retrieving factually grounded responses.

### ⚙️ Architecture
1️⃣ Document Processing & Vectorization
📂 PDF Loader: Extracts text from research papers (PyPDFDirectoryLoader).
🧩 Text Splitting: Uses RecursiveCharacterTextSplitter (1k tokens, 200 overlap) for optimal chunking.
🧠 Embedding Generation: Converts text into dense vectors using sentence-transformers/all-MiniLM-L6-v2.
📌 FAISS Indexing: Stores embeddings for fast nearest-neighbor retrieval.
2️⃣ Retrieval-Augmented Generation (RAG) Pipeline
🔎 Query Processing: Converts user input into vector space.
📑 Context Retrieval: Matches against FAISS vectors to fetch top-k relevant chunks.
🤖 LLM-Based Answering: Feeds retrieved context into Mixtral-8x7B via LangChain for precise, context-grounded responses.
3️⃣ Interactive UI (Streamlit)
⚡ Real-time Q&A with dynamic document embedding.
📌 Similarity Search Visualization for transparency.
⏳ Response Time Tracking using Python’s time.process_time().
🔗 Tech Stack
✅ Python | Streamlit | LangChain | FAISS | Hugging Face | Groq API

### 🚀 Future Enhancements
🔹 Hybrid Search (BM25 + Dense Retrieval) for better relevance.
🔹 Multi-turn Conversations with memory augmentation.
🔹 Fine-tuned LLMs for specialized research domains.
💡 Why It Matters
Traditional keyword-based search lacks semantic depth. This RAG system bridges the gap by ensuring factually accurate, explainable, and efficient information retrieval from research papers.
