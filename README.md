# Chatbot-For-Analyzing-PDF
It analyzes the pdf and gives the responses
📌 Project: Flask-based AI Chatbot Backend

This project is a Flask-powered backend API designed to support an AI chatbot with two core capabilities:

Interactive Chat Handling – Processes user queries and generates intelligent responses.

Document Processing – Accepts uploaded PDF/text documents, analyzes their content, and allows users to ask context-based questions.

⚙️ Features

REST API Endpoints

/process-message → Accepts a user message and returns a chatbot-generated response.

/process-document → Accepts and processes an uploaded file (e.g., PDF) for knowledge extraction.

/ → Serves the front-end interface (index.html).

CORS Support → Ensures smooth integration with frontend applications.

Worker Integration → Delegates heavy AI/NLP tasks (e.g., prompt processing, document parsing) to a separate worker.py module.

Error Handling → Handles invalid file uploads gracefully.

Cross-platform Deployment → Runs on 0.0.0.0:8000 for local or containerized environments.

🏗️ Tech Stack

Backend: Flask (Python)

CORS: Flask-CORS

Logging: Python logging

Worker Module: Custom Python module (worker.py) for AI/NLP processing

🚀 API Usage
1️⃣ Process User Message

Endpoint:

POST /process-message


Request (JSON):

{
  "userMessage": "What is AI?"
}


Response:

{
  "botResponse": "AI stands for Artificial Intelligence..."
}

2️⃣ Process Document Upload

Endpoint:

POST /process-document


Request (Form-Data):

file: PDF/Text file

Response:

{
  "botResponse": "Thank you for providing your PDF document. I have analyzed it, so now you can ask me any questions regarding it!"
}

📂 Project Structure
project/
│── app.py              # Main Flask application
│── worker.py           # Worker module for AI/NLP logic
│── templates/
│   └── index.html      # Frontend UI
│── requirements.txt    # Python dependencies

⚡ Run Locally
# Clone repo
git clone https://github.com/your-username/your-repo.git
cd your-repo

# Install dependencies
pip install -r requirements.txt

# Run server
python app.py


Server runs on → http://localhost:8000/

📦 Deployment

Can be deployed on Heroku, Docker, AWS, or any cloud VM.

Exposes API on port 8000 for external access.

🔮 Future Enhancements

Add authentication for secured API access

Support multiple document formats (Word, Excel, etc.)

Integration with vector databases for semantic search

Real-time streaming chatbot responses
