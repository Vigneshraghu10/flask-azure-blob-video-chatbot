# flask-azure-blob-video-chatbot
This project is a simple chatbot built with Flask that matches user questions to video resources stored in Azure Blob Storage. It uses fuzzy matching to find the best question and generates secure SAS URLs for accessing videos.

## Features
- Accepts user questions and finds the best-matched answer using fuzzy matching.
- Provides secure access to videos hosted in Azure Blob Storage via SAS URLs.
- Simple web-based interface for user interaction.

## Requirements
- Python 3.x
- Flask
- Azure Blob Storage account
- FuzzyWuzzy library for text matching

## Usage

1. Start the Flask app:
    ```bash
    python app.py
    ```
2. Open the app in your browser at `http://127.0.0.1:5000/`.

3. Ask a question in the chat interface, and the app will return a video URL if a match is found.

### Example Workflow
- User enters: "What is machine learning?"
- App finds the best match ("What is machine learning?") and returns a secure video link to the corresponding blob.

## Security Best Practices
- Store sensitive information like `AZURE_CONNECTION_STRING` in environment variables or a secure configuration file.
- Use role-based access control (RBAC) for your Azure Blob Storage account.

## Dependencies
- **Flask**: Web framework for building the chatbot.
- **Azure Storage Blob**: SDK for interacting with Azure Blob Storage.
- **FuzzyWuzzy**: Library for fuzzy string matching.

Install all dependencies with:
```bash
pip install -r requirements.txt

