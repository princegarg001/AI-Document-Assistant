# Use official Python image
FROM python:3.10

# Set working directory
WORKDIR /app

# Install system dependencies for faiss-cpu, PyMuPDF, pytesseract (with debug)
RUN apt-get update && \
    apt-get install -y --no-install-recommends \
        tesseract-ocr \
    || (cat /var/log/apt/term.log && false)

# Copy requirements and install dependencies
COPY requirements.txt ./
RUN pip install --no-cache-dir -r requirements.txt

# Copy the rest of the app
COPY . .

# Expose the port Gradio will run on
EXPOSE 7860

# Run the Gradio app
CMD ["python", "gradio_app.py"]
