# 🎥 YouTube Video Chatbot (Phase 1)

An AI-powered chatbot that allows users to chat with any YouTube video. The system extracts video transcripts, converts them into embeddings, stores them in a vector database, and uses Retrieval-Augmented Generation (RAG) to provide accurate, context-aware answers based on the video content.

---

## 🚀 Project Overview

Learning from YouTube videos can be challenging when users need quick answers to specific questions. Instead of manually searching through long videos, this application enables users to ask questions directly and receive answers grounded in the video's transcript.

The chatbot leverages Large Language Models (LLMs) and RAG architecture to understand video content and provide intelligent responses.

---

## ✨ Features

* Enter any YouTube video URL
* Extract video transcripts automatically
* Split transcripts into manageable chunks
* Generate semantic embeddings
* Store embeddings in a vector database
* Retrieve relevant content using similarity search
* Generate context-aware answers using an LLM
* Display source context used for answering
* Simple and interactive user interface

---

## 🏗️ Architecture

YouTube URL
    │
    ▼
Transcript Extraction        ← youtube-transcript-api (free)
    │
    ▼
Text Chunking                ← LangChain TextSplitter
    │
    ▼
Embedding Generation         ← HuggingFace (free) or Gemini (free tier)
    │
    ▼
Vector Store (ChromaDB)      ← local, free
    │
    ▼
Similarity Search
    │
    ▼
Retrieved Context
    │
    ▼
LLM Answer Generation        ← Groq (free tier) / Ollama (local, free)
    │
    ▼
Response to User             ← Streamlit UI


---

## 🛠️ Tech Stack

┌─────────────────────────────────────────────┐
│              User Interface                  │
│           Streamlit / Gradio                 │
├─────────────────────────────────────────────┤
│                Backend                       │
│              FastAPI (Phase 5)               │
├──────────────────┬──────────────────────────┤
│   RAG Pipeline   │      LLM Layer            │
│   LangChain      │  Groq (free) /            │
│   ChromaDB       │  Ollama (local, free)     │
│   sentence-      │                           │
│   transformers   │                           │
├──────────────────┴──────────────────────────┤
│             Data Source                      │
│         youtube-transcript-api               │
└─────────────────────────────────────────────┘

* YouTube Transcript API

---

## 📂 Project Structure

youtube-video-chatbot/
│
├── app.py
├── requirements.txt
├── .env
│
├── data/
│
├── src/
│   ├── transcript_loader.py
│   ├── text_splitter.py
│   ├── embeddings.py
│   ├── vector_store.py
│   ├── retriever.py
│   └── chatbot.py
│
└── README.md

---

## 🔄 Workflow

### Step 1

User enters a YouTube video URL.

### Step 2

The application extracts the transcript from the video.

### Step 3

The transcript is divided into smaller chunks.

### Step 4

Embeddings are generated for each chunk.

### Step 5

Embeddings are stored in ChromaDB.

### Step 6

The user asks a question.

### Step 7

Relevant transcript chunks are retrieved using semantic similarity.

### Step 8

The retrieved context is sent to the LLM.

### Step 9

The LLM generates an accurate answer based on the video content.

---

## 📸 Example

### Input

```text
YouTube URL:
https://youtube.com/example-video

Question:
What is Retrieval-Augmented Generation?
```

### Output

```text
Retrieval-Augmented Generation (RAG) is a technique that
combines information retrieval with large language models
to generate accurate and context-aware responses.
```

---

## 🎯 Learning Objectives

This project demonstrates:

* Retrieval-Augmented Generation (RAG)
* Embedding Models
* Vector Databases
* Semantic Search
* LangChain Framework
* Prompt Engineering
* LLM Integration
* Streamlit Application Development

---

## 🔮 Future Improvements

* Playlist support
* Timestamp-based Q&A
* Voice interaction
* Conversation memory
* Personalized learning assistant

---

## 🤝 Contributing

Contributions, issues, and feature requests are welcome.

Feel free to fork the repository and submit a pull request.

---

## 📜 License

This project is licensed under the MIT License.

---

## 👨‍💻 Author

**Anubhav Kesharwani**

Exploring:

* Generative AI
* Agentic AI
* RAG Systems
* LangChain
* AI-Powered Learning Applications
