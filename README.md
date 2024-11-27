# Docu-LM: Multi-Modal Document Retrieval and Analysis System

## Overview

Docu-LM is an advanced document retrieval and analysis application that leverages Retrieval-Augmented Generation (RAG) architecture with multi-modal capabilities. The system allows users to upload documents and interact with an intelligent chatbot that can extract and analyze contextual information from complex multi-page documents, including visual elements like charts and graphs.

## Key Features

- **Page-Level Indexing**: Implement precise document retrieval using ColPali
- **Multi-Modal Analysis**: Analyze text, charts, and graphs together
- **Intelligent Chatbot**: Powered by GPT-4o-mini for comprehensive answers
- **React Frontend**: User-friendly interface for document upload and interaction
- **Caching Mechanism**: Redis-based response caching for improved performance

## Prerequisites

Before setting up the project, ensure you have the following:

- Python 3.8+
- Node.js and npm
- Redis Server
- OpenAI API Key

## Installation and Setup

### Backend Setup

1. Clone the repository:
   ```bash
   git clone https://github.com/vedantmehta14/Docu-LM
   cd Docu-LM
   ```

2. Create a virtual environment:
   ```bash
   python3 -m venv venv
   source venv/bin/activate  # On Windows, use `venv\Scripts\activate`
   ```

3. Install Python dependencies:
   ```bash
   pip install -r requirements.txt
   ```

4. Set up OpenAI API Key:
   ```bash
   export OPENAI_API_KEY='your_openai_api_key_here'
   ```
   **Note**: Replace `your_openai_api_key_here` with your actual OpenAI API key.

5. Install Redis:
   - macOS (using Homebrew): `brew install redis`
   - Ubuntu/Debian: `sudo apt-get install redis-server`
   - Windows: Download from [Redis Official Website](https://redis.io/download)

### Frontend Setup

1. Navigate to the frontend directory:
   ```bash
   cd frontend
   ```

2. Install npm dependencies:
   ```bash
   npm install
   ```

## Running the Application

### Start Redis Server

```bash
# macOS/Linux
redis-server

# Windows
redis-cli
```

### Start Backend Server

```bash
# Activate virtual environment
source venv/bin/activate  # On Windows, use `venv\Scripts\activate`

# Run Flask server
python app.py
```

### Start React Frontend

```bash
cd frontend
npm start
```

## Configuration Notes

- Update `app.py`:
  - Set correct path for PDF file
  - Replace `RAGMultiModalModel.from_index()` with your index path
  - Set `OPENAI_API_KEY` environment variable

- Modify `app.jsx`:
  - Adjust backend URL if not running on `http://localhost:8000`

## Dependencies

### Python
- Flask
- Flask-CORS
- pdf2image
- redis
- openai
- byaldi (custom RAG library)

### JavaScript
- React
- Axios/Fetch for API calls

## Troubleshooting

- Ensure Redis server is running
- Verify OpenAI API key is valid
- Check network connectivity
- Validate PDF document path

## Contact

Vedant Mehta - mehtavedant8@gmail.com
