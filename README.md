# 📝 RAG Chat Assistant

[![Python](https://img.shields.io/badge/Python-3.10+-blue?logo=python)](https://www.python.org/) 
[![Flask](https://img.shields.io/badge/Flask-2.3-green?logo=flask)](https://flask.palletsprojects.com/) 
[![Gradio](https://img.shields.io/badge/Gradio-3.42-orange?logo=gradio)](https://gradio.app/) 
[![Docker](https://img.shields.io/badge/Docker-24.0-blue?logo=docker)](https://www.docker.com/) 
[![FAISS](https://img.shields.io/badge/FAISS-1.7-lightgrey)](https://faiss.ai/)  

_A Retrieval-Augmented Generation (RAG) application to upload PDFs, text files, and images and chat with them to get source-backed answers._

---

## 🚀 Features

- **File Upload:** PDFs, text files, images (PNG, JPG, TIFF)  
- **Automatic OCR:** Extract text from scanned PDFs and images  
- **Vector Indexing:** Searchable knowledge base using FAISS  
- **Chat Interface:** Ask questions and get answers from your documents  
- **Source Citations:** Answers include references to the original document and page  

---

## 🗂️ Project Structure

**Day 1 & Day 2** – Basics of:  

- PDF and image uploads  
- Text chunking  
- Vector store creation  
- End-to-end RAG flow  

**Day 3 – Full RAG Chat Assistant**  

**Backend (Flask)**  

- File processing  
- OCR for scanned documents/images  
- Text chunking & vector indexing  
- RAG chain for answering queries  

**Frontend (Gradio)**  

- User-friendly web interface for file uploads and chat  
- Source-backed responses  

---

## 🛠️ Local Setup

**Backend**

```bash
# Navigate to project directory
python -m venv .venv       # optional
source .venv/bin/activate  # Windows: .venv\Scripts\activate
pip install -r requirements.txt
python app.py               # Runs at http://localhost:8000
Frontend

bash
Copy code
# In a new terminal
source .venv/bin/activate  # if using virtual environment
python gradio_app.py        # Runs at http://127.0.0.1:7860
🐳 Docker Deployment
bash
Copy code
# Build Docker Image
docker build -t rag-chat-assistant .

# Run Container
docker run -p 8000:8000 -p 7860:7860 rag-chat-assistant
Backend → http://localhost:8000

Frontend → http://localhost:7860

☁️ Deploy on Render
Push your repository to GitHub

Create a Web Service on Render for the backend:

Connect your GitHub repo

Build Command: docker build -t rag-backend .

Start Command: docker run -p 8000:8000 rag-backend

Repeat for the frontend service

✅ Your RAG Chat Assistant is live via Render URLs!

Live Site: [Add your live site URL here]

📂 Supported File Types
PDFs (.pdf)

Text files (.txt)

Images (.png, .jpg, .jpeg, .tiff)

💡 Usage
Check backend status in the Gradio UI

Upload files in the Upload Files tab and click Index

Chat in the Chat tab and get answers with source citations

⚡ Technologies
Python, Flask, Gradio

Tesseract OCR

FAISS vector search

PyPDF2, Pillow for document handling

Docker & Render for deployment

LLM integration for RAG

🎬 Demo
https://ai-document-assistant-1.onrender.com
