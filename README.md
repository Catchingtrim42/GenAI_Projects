Minimalist PDF RAG Assistant:

An end-to-end Retrieval-Augmented Generation (RAG) system built with LangChain, Hugging Face Embeddings, Groq LLM (openai/gpt-oss-120b), and an interactive Gradio UI featuring a minimalist dark theme.
📌 Overview
This project provides a complete pipeline to upload PDF documents, generate vector embeddings, store them in a vector database (ChromaDB / FAISS), and query the document context using a high-performance LLM provided via Groq. It includes both programmatic RAG chain execution and a web-based chat interface.
✨ Features
* PDF Processing & Chunking: Parses PDFs using PyPDFLoader and splits documents into optimized text chunks using RecursiveCharacterTextSplitter.
* Vector Embeddings: Generates dense semantic vector embeddings using Hugging Face's sentence-transformers/all-MiniLM-L6-v2.
* Dual Vector Store Options: Supports indexing with ChromaDB and FAISS.
* Groq LLM Integration: Uses ChatGroq (openai/gpt-oss-120b) for rapid inference and response generation based strictly on document context.
* Custom Gradio Web Interface: Features a custom dark/monochrome UI (gr.Blocks) with adjustable top-$k$ retrieval sliders, document status indicators, and chat history management.
🛠️ Tech Stack & Dependencies
Layer
	Technology
	Framework
	LangChain Core / Community / Groq / Chroma / HuggingFace
	LLM Inference
	Groq API (openai/gpt-oss-120b)
	Embeddings
	Hugging Face (sentence-transformers/all-MiniLM-L6-v2)
	Vector DB
	ChromaDB / FAISS
	PDF Loader
	PyPDF (PyPDFLoader)
	User Interface
	Gradio
	🚀 Getting Started
1. Prerequisites & Installation
Ensure you have Python 3.9+ installed. Install all required packages:






Bash
pip install -q -U langchain langchain-core langchain-groq langchain-community \
               langchain-chroma langchain-huggingface langchain-text-splitters \
               chromadb faiss-cpu sentence-transformers gradio pypdf

2. API Key Configuration
Set your Groq API key in your environment variables or Google Colab Secrets (GenIntel):






Python
import os
import getpass

os.environ["GROQ_API_KEY"] = getpass.getpass("Enter your Groq API key: ")

⚙️ How It Works
1. Document Loading & Splitting:
   * PDFs are loaded via PyPDFLoader.
   * Text is split into chunks ($300$–$500$ characters with a $50$-character overlap).
2. Embedding & Vector Storage:
   * Chunks are transformed into vector representations using all-MiniLM-L6-v2.
   * Embeddings are persisted in vector stores (Chroma or FAISS).
3. Retrieval Chain:
   * Queries retrieve top matching document chunks ($k=3$ by default).
   * Formatted context is supplied to ChatGroq with strict instructions to answer only from context.
4. Gradio Deployment:
   * Launch interactive web applications via app.launch(share=True).
💻 Running the Project
Run the Python script directly:






Bash
python rag_02.py

Once launched, open the local or public Gradio URL output in your terminal/notebook to interact with the document assistant.
