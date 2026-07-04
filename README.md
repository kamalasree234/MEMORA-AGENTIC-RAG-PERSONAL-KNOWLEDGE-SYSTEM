# 🧠 MEMORA - AGENTIC RAG PERSONAL KNOWLEDGE SYSTEM

<p align="center">
  <b>An AI-powered Personal Knowledge Management System built using Agentic RAG, LangGraph, Hybrid Retrieval, and Machine Learning.</b>
  <br><br>
  Transform your study materials into an intelligent learning assistant capable of answering questions, generating flashcards, quizzes, and personalized revision schedules—all grounded strictly in your own knowledge base.
</p>

---

## 📌 Overview

**Memora** is an AI-powered personal knowledge system designed to help students and lifelong learners organize, retrieve, and learn from their own study materials.

Unlike conventional AI chatbots that rely heavily on a language model's pre-trained knowledge, Memora follows an **Agentic Retrieval-Augmented Generation (RAG)** approach. Every response is generated **strictly from user-uploaded documents**, ensuring reliable, context-aware, and source-grounded answers while significantly reducing hallucinations.

The system supports uploading **PDFs, URLs, and YouTube videos**, converts them into searchable embeddings, retrieves the most relevant information using **hybrid dense + sparse retrieval**, and employs a **LangGraph-powered multi-agent workflow** to intelligently process every query before generating a response.

Additionally, Memora integrates an **XGBoost-based forgetting prediction model** that analyzes user learning behavior and recommends adaptive revision schedules through spaced repetition, making studying more personalized and efficient.

---

## ✨ Key Features

### 📄 Knowledge Ingestion

- Upload PDF notes and textbooks
- Import content from URLs
- Process YouTube video transcripts
- Automatic text extraction and chunking
- Metadata preservation for accurate citations

---

### 🤖 Agentic RAG Pipeline

Unlike traditional RAG systems, Memora uses a multi-agent workflow powered by **LangGraph**.

The pipeline consists of:

- Query Routing
- Hybrid Document Retrieval
- Relevance Grading
- Query Rewriting
- Context Validation
- Grounded Response Generation

This enables the system to retrieve only the most relevant information before generating answers.

---

### 🔍 Hybrid Retrieval

Memora combines **semantic search** with **keyword-based retrieval** for improved accuracy.

- Dense Vector Search
- Sparse Keyword Search
- Hybrid Ranking
- Context Filtering

This approach performs significantly better than standalone semantic search, especially for technical notes, formulas, and short study materials.

---

### 💬 Conversational AI Assistant

Interact with your personal knowledge base naturally.

Examples:

- Explain this concept
- Summarize Chapter 5
- Compare CNN and RNN
- Give real-world examples
- Generate interview questions
- Test my understanding

Every response is generated using only retrieved document context.

---

### 📚 AI Learning Tools

Memora automatically creates:

- Flashcards
- Adaptive quizzes
- Topic summaries
- Revision notes
- Concept explanations

---

### 📊 Learning Analytics

Track your learning progress through analytics such as:

- Study duration
- Quiz performance
- Frequently revised topics
- Weak areas
- Learning consistency
- Revision history

---

### 🧠 Machine Learning-Based Revision Planner

Memora uses an **XGBoost** model trained on study behavior data to estimate the probability of forgetting each topic.

The model considers:

- Review frequency
- Quiz accuracy
- Session duration
- Time since last revision
- Learning consistency

Based on these predictions, the system recommends personalized revision schedules using adaptive spaced repetition.

---

## 🏗️ System Architecture

```text
                           User
                             │
          Upload PDFs / URLs / YouTube Videos
                             │
                  Document Processing Pipeline
       (Extraction → Cleaning → Chunking → Metadata)
                             │
               Gemini Embedding Generation
                             │
                  Qdrant Vector Database
          (Hybrid Dense + Sparse Retrieval)
                             │
                 LangGraph Agent Workflow
        ┌──────────────────────────────────────┐
        │ Query Router                         │
        │ Hybrid Retriever                     │
        │ Relevance Grader                     │
        │ Query Rewriter                       │
        │ Context Validator                    │
        └──────────────────────────────────────┘
                             │
                  Gemini Large Language Model
                             │
          Grounded AI Response with Citations
                             │
Flashcards • Quizzes • Learning Analytics • Revision Planner
```

---

## ⚙️ Workflow

1. Users upload learning materials.
2. Documents are cleaned and divided into semantic chunks.
3. Each chunk is converted into vector embeddings.
4. Embeddings are stored inside the Qdrant vector database.
5. A user submits a question.
6. LangGraph routes the query through multiple intelligent agent nodes.
7. Hybrid retrieval fetches the most relevant document chunks.
8. Retrieved chunks are evaluated using a relevance grader.
9. If retrieval quality is low, the query is automatically rewritten.
10. Gemini generates a grounded response using only validated context.
11. The answer is returned with supporting citations.

---

## 🛠️ Tech Stack

### Frontend

- React
- TypeScript
- Tailwind CSS
- Vite

### Backend

- Node.js
- Express.js
- MongoDB Atlas

### AI & Machine Learning

- LangGraph
- LangChain
- Google Gemini API
- Gemini Embeddings
- Qdrant Vector Database
- XGBoost
- Scikit-learn
- Pandas
- NumPy

### Agent Microservice

- FastAPI
- Python

---

## 📂 Project Structure

```bash
Memora/
│
├── client/                 # React + TypeScript frontend
├── server/                 # Node.js + Express backend
├── agent-service/          # FastAPI + LangGraph orchestration
├── ml-model/               # XGBoost model training & inference
├── uploads/                # User uploaded documents
├── docs/                   # Documentation
├── README.md
└── LICENSE
```

---

## 🚀 Future Enhancements

- 🖼️ OCR support for handwritten notes
- 🌍 Multi-language document understanding
- 🤝 Collaborative knowledge workspaces
- 📅 Calendar-integrated revision planning
- 📈 Advanced learning analytics and forecasting
- 🎙️ Voice-based conversational learning assistant
- 📑 Research paper understanding and citation support

---

## 👨‍💻 Author

**Kamalasree S.**

---

## ⭐ Support

If you found this project helpful, consider giving it a **⭐ Star** on GitHub. Your support helps the project reach more developers and learners!

---

> **Memora** aims to make AI-assisted learning more reliable, personalized, and explainable by combining Agentic RAG, hybrid retrieval, and machine learning into a unified knowledge management platform.
