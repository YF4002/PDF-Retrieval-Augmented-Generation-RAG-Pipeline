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

DEMO:
- In this example, I processed a Spring Semester Scheduling Worksheet through the system. When queried, the model provided accurate and relevant responses.

<img width="891" height="609" alt="Image" src="https://github.com/user-attachments/assets/3016ce68-6043-4038-9966-71a7279b2670" />

<img width="890" height="365" alt="Image" src="https://github.com/user-attachments/assets/f0a80857-662e-4124-a903-f2fb375abc88" />

<img width="887" height="672" alt="Image" src="https://github.com/user-attachments/assets/29be636f-3715-42ed-a04d-18ec8d6d1382" />
