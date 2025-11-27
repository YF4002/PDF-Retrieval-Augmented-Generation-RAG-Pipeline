PDF RAG Chatbot — Intelligent Document Q&A System

Tired of digging through long PDFs? This tool makes your documents talk back.

A lightweight, AI-powered tool that transforms static PDFs into interactive, searchable knowledge. Upload any document, contracts, reports, invoices, or even scanned paperwork, and instantly turn it into an interactive AI assistant where you can ask questions directly like you would with a human expert.

Powered by a RAG pipeline that combines:

- PyMuPDF + Tesseract OCR to read both digital and scanned PDFs

- MiniLM embeddings + FAISS for high-speed semantic search

- FLAN-T5 for grounded, citation-backed answers

The Gradio interface offers a simple experience: upload → index → chat.
Perfect for anyone who needs quick insights from large or messy documents without manually searching page by page.


Languages / Stack

- Python, FAISS, PyMuPDF, Tesseract OCR, Gradio, Sentence-Transformers, Transformers (FLAN-T5)
