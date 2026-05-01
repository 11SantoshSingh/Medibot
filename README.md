Optimizing tool selection...

Read [](file:///c%3A/Users/SANTOSH/OneDrive/Documents/GitHub/Medibot/app.py#1-1), lines 1 to 50

Read [](file:///c%3A/Users/SANTOSH/OneDrive/Documents/GitHub/Medibot)

Read [](file:///c%3A/Users/SANTOSH/OneDrive/Documents/GitHub/Medibot/src)

Read [](file:///c%3A/Users/SANTOSH/OneDrive/Documents/GitHub/Medibot/data)

Read [](file:///c%3A/Users/SANTOSH/OneDrive/Documents/GitHub/Medibot/store_index.py)

Read [](file:///c%3A/Users/SANTOSH/OneDrive/Documents/GitHub/Medibot/requirements.txt)

Read [](file:///c%3A/Users/SANTOSH/OneDrive/Documents/GitHub/Medibot/README.md#1-1), lines 1 to 50

Read [](file:///c%3A/Users/SANTOSH/OneDrive/Documents/GitHub/Medibot/src/prompt.py)

Read [](file:///c%3A/Users/SANTOSH/OneDrive/Documents/GitHub/Medibot/src/helper.py)

# Medibot: Medical Chatbot Project Summary

## 📋 Project Overview

**Medibot** is a medical chatbot application built with modern AI technologies that provides intelligent responses to medical queries using Retrieval-Augmented Generation (RAG). The system processes medical documents and uses vector search to provide contextually relevant answers.

## 🏗️ Architecture & Tech Stack

### Core Technologies:
- **Backend**: Flask (Python web framework)
- **AI/ML**: LangChain, Google Gemini AI, HuggingFace Embeddings
- **Vector Database**: Pinecone (for semantic search)
- **Embeddings**: Sentence Transformers (all-MiniLM-L6-v2 model)
- **Document Processing**: PyPDF for PDF parsing, RecursiveCharacterTextSplitter for text chunking

### Key Components:
1. **Document Ingestion**: Loads and processes medical PDFs and text files
2. **Vector Embeddings**: Converts text chunks into 384-dimensional vectors
3. **Vector Search**: Semantic search using Pinecone for relevant context retrieval
4. **LLM Integration**: Google Gemini AI for generating responses
5. **Web Interface**: Flask-based chat interface

## 📁 Project Structure

```
Medibot/
├── app.py                 # Main Flask application
├── store_index.py         # Script to create and populate Pinecone index
├── requirements.txt       # Python dependencies
├── README.md             # Project documentation
├── data/                 # Medical documents (PDFs and text files)
│   ├── Medical_book.pdf
│   ├── faq.txt
│   ├── hospital_app.txt
│   └── pneumonia.txt
├── src/                  # Source code modules
│   ├── helper.py         # Utility functions for data processing
│   ├── prompt.py         # System prompts for the chatbot
│   └── __init__.py
├── templates/            # HTML templates for the web interface
├── research/             # Research and experimentation notebooks
│   └── trials.ipynb      # Jupyter notebook for testing components
└── static/               # Static assets (CSS, JS, images)
```

## 🚀 Quick Start Guide

### Prerequisites:
- Python 3.10+
- Conda (recommended for environment management)
- API keys for Pinecone and Google Gemini AI

### Installation Steps:

1. **Clone the repository:**
```bash
git clone https://github.com/entbappy/Build-a-Complete-Medical-Chatbot-with-LLMs-LangChain-Pinecone-Flask-AWS.git
cd Medibot
```

2. **Create and activate conda environment:**
```bash
conda create -n medibot python=3.10 -y
conda activate medibot
```

3. **Install dependencies:**
```bash
pip install -r requirements.txt
```

4. **Set up environment variables:**
Create a .env file in the root directory:
```ini
PINECONE_API_KEY=your_pinecone_api_key_here
GEMINI_API_KEY=your_gemini_api_key_here
```

5. **Create the vector index:**
```bash
python store_index.py
```

6. **Run the application:**
```bash
python app.py
```

7. **Access the chatbot:**
Open your browser and go to `http://localhost:8080`

## 🔧 Key Features

### Document Processing:
- Supports PDF and text file ingestion
- Intelligent text chunking (500 characters with 20-character overlap)
- Metadata preservation for source tracking

### AI Capabilities:
- Semantic search using vector embeddings
- Context-aware responses using RAG
- Medical domain specialization
- Concise, medically-focused answers

### Web Interface:
- Clean chat interface
- Real-time conversation
- Responsive design

## 📊 Data Flow

1. **Ingestion**: Medical documents → Text extraction → Chunking
2. **Indexing**: Text chunks → Vector embeddings → Pinecone storage
3. **Query Processing**: User question → Vector search → Context retrieval
4. **Response Generation**: Context + Question → Gemini AI → Answer

## 🔑 API Keys Required

- **Pinecone API Key**: For vector database operations
- **Google Gemini API Key**: For LLM-powered responses

## 🐛 Common Issues & Solutions

### API Quota Limits:
- Gemini free tier: 20 requests/day
- Solution: Upgrade to paid plan or wait for reset

### Missing Dependencies:
- Ensure all packages in requirements.txt are installed
- Use the specified Python version (3.10)

### Environment Variables:
- Ensure .env file exists with correct API keys
- Restart the application after changing environment variables

## 🎯 Use Cases

- Medical information retrieval
- Hospital service inquiries
- General health-related Q&A
- Educational tool for medical students

## 🔄 Development Workflow

1. **Experiment**: Use trials.ipynb for testing components
2. **Index Data**: Run store_index.py to update the vector database
3. **Develop**: Modify app.py for backend changes, src for utilities
4. **Test**: Run the Flask app and interact via web interface

This project demonstrates a complete RAG pipeline from document ingestion to web deployment, making it an excellent learning resource for AI-powered applications.