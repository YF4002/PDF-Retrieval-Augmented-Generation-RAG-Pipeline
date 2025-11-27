PDF Retrieval-Augmented Generation (RAG) Chatbot

A production-ready Retrieval-Augmented Generation (RAG) system for querying unstructured PDF documents through a conversational interface.
The application extracts text (including OCR for scanned PDFs), performs semantic chunking and vector indexing, retrieves relevant context using FAISS, and generates grounded answers using a FLAN-T5-based RAG pipeline.

Built with Python, Gradio, PyMuPDF, Tesseract OCR, Sentence-Transformers, FAISS, and Transformers.

🔹 Key Capabilities
1. Robust PDF Processing

Extracts structured text using PyMuPDF.

Automatically performs OCR via Tesseract for scanned or image-based PDFs.

Supports multi-page, noisy, or irregular enterprise documents.

2. Semantic Chunking + Metadata Tracking

Overlapping text chunking for higher retrieval accuracy.

Per-chunk metadata stored:

Page number

Document type (Invoice / Report / Contract / General)

Source identifiers

3. Vector Embedding + FAISS Search

Encodes text using all-MiniLM-L6-v2 embeddings.

Stores vectors in a FAISS L2 index for fast nearest-neighbor retrieval.

Retrieves top-k most relevant chunks with relevance scoring.

4. RAG-Driven Answer Generation

FLAN-T5 synthesizes answers only from retrieved context.

Provides:

Full natural-language answer

Cited page numbers and document types

Relevance metadata

A confidence score

5. Clean, Modern User Interface

Built with Gradio, including:

Upload Tab for document ingestion

Chat Tab with searchable conversation history

One-click clearing and real-time result streaming

📂 Repository Structure
pdf-rag-chatbot/
│
├── app.py                # Main RAG pipeline and Gradio UI
├── README.md
├── requirements.txt
└── assets/
    └── examples/         # Optional sample PDFs or screenshots

🔧 Installation & Setup
Install Python Dependencies
pip install gradio pypdf PyMuPDF pytesseract pillow faiss-cpu sentence-transformers transformers accelerate

Install Tesseract OCR (Required for scanned PDFs)

macOS

brew install tesseract


Ubuntu/Debian

sudo apt install tesseract-ocr


Windows
Download installer from: https://github.com/UB-Mannheim/tesseract/wiki

▶️ Running the Application
python app.py


Gradio will launch locally and provide a public share link when running on Colab or supported environments.

🧠 System Architecture Overview
1. Ingestion Pipeline

Accepts PDF files (binary input)

Performs text extraction or OCR

Classifies document type based on content

Splits content into semantic chunks

2. Embedding + Indexing

Generates vector embeddings for each chunk

Builds a FAISS L2 index for similarity search

Stores metadata alongside vectors

3. Retrieval

Encodes user query

Retrieves top-k most relevant chunks

Computes relevance and confidence scores

4. Generation

Constructs a context-aware prompt

Sends prompt to FLAN-T5 for grounded answer generation

Formats final output with:

Answer

Sources

Relevance scores

Confidence score

5. User Interface

Real-time chat interface

Persistent conversation state

Upload + preprocessing workflow

💬 Example Use Cases

Contract clause search

Invoice summarization

Report analysis

Business intelligence Q&A

Enterprise knowledge extraction

Document automation workflows

📜 License

MIT License — unrestricted use for personal and commercial applications.
