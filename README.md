Day 1 & Day 2

Basics of:

PDF and image uploads

Text chunking

Vector store creation

End-to-end RAG flow

Day 3 – RAG Chat Assistant

Full-featured RAG application with:

Flask Backend – File processing, OCR, text chunking, vector indexing, RAG chain

Gradio Frontend – User-friendly interface for file uploads and chat with source-backed responses

✨ Features

File Upload: PDFs, text files, and images (PNG, JPG, TIFF)

Automatic OCR: Extract text from images and scanned PDFs

Vector Indexing: Searchable knowledge base using FAISS

Chat Interface: Ask questions about your documents

Source Citations: Answers include references to original documents/pages

🛠️ Local Setup & Running

You need two terminal windows for backend and frontend.

1️⃣ Backend Server
# Navigate to project directory
python -m venv .venv           # Optional virtual environment
source .venv/bin/activate       # Windows: .venv\Scripts\activate

pip install -r requirements.txt
python app.py                   # Backend runs at http://localhost:8000

2️⃣ Frontend UI
# In a new terminal
source .venv/bin/activate       # If using virtual environment
python gradio_app.py            # Gradio UI runs at http://127.0.0.1:7860

🚀 Usage

Check Backend Status – Ensure frontend is connected

Upload Files – Drag & drop PDFs/images in the Upload Files tab, then click Index

Chat – Go to Chat tab, ask a question, press Enter, and see answers with sources

🐳 Docker Deployment

The project is fully Dockerized, allowing easy deployment:

Build Docker Image
docker build -t rag-chat-assistant .

Run Container
docker run -p 8000:8000 -p 7860:7860 rag-chat-assistant


Backend → http://localhost:8000

Frontend → http://localhost:7860

☁️ Deploy on Render

Push your repository to GitHub

Create a new Web Service on Render for the backend:

Connect your GitHub repo

Set Build Command: docker build -t rag-backend .

Set Start Command: docker run -p 8000:8000 rag-backend

Create a new Web Service for the frontend similarly:

Connect to the same repo

Build & run frontend container

✅ Your RAG Chat Assistant is now live and accessible via the Render URLs!

🧩 Technologies Used

Python, Flask, Gradio

OCR: Tesseract

Vector Search: FAISS

Document Handling: PyPDF2, Pillow

LLM Integration for RAG

Docker for containerization

Render for cloud deployment

📂 Supported Files

PDFs (.pdf)

Text files (.txt)

Images (.png, .jpg, .jpeg, .tiff)

📖 Example Workflow

Upload PDF & images

Index files into FAISS vector store

Ask questions: “What is the revenue growth in Q2?”

Receive answers with source citations
