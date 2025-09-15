# Example backend Dockerfile
FROM python:3.10
WORKDIR /app
COPY . .
RUN pip install --no-cache-dir \
	flask \
	flask-cors \
	PyMuPDF \
	google-generativeai \
	pytesseract \
	python-dotenv \
	langchain \
	langchain-community \
	langchain-google-genai \
	langchain-experimental \
	Pillow
EXPOSE 8000
CMD ["python", "app.py"]
