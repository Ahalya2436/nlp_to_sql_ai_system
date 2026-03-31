# NL to SQL AI System

An end-to-end AI-powered system that converts natural language queries into SQL using LLM (LLaMA), RAG-based schema retrieval, and intelligent retry mechanisms.

---

## Overview

This project enables users to query databases using natural language.  
The system translates user input into optimized SQL queries, executes them, and returns results along with evaluation metrics.

---

## Key Features

-  Natural Language → SQL conversion
-  LLM-powered query generation (LLaMA via vLLM / GPU)
-  Schema Retrieval using RAG (Vector DB - Qdrant)
-  Smart Schema Filtering (reduces hallucination)
-  Retry Mechanism (auto-fix SQL errors)
-  Evaluation Metrics:
  - Success rate
  - Retry count
  - Execution time
  - Hallucination detection
-  Power BI Dashboard for monitoring
-  FastAPI backend + Streamlit UI

---

## Architecture
User (Streamlit UI)
↓
FastAPI API (/query/ask)
↓
Schema Retrieval (RAG - Qdrant)
↓
Schema Filtering
↓
LLM (LLaMA - GPU via vLLM)
↓
SQL Generation
↓
SQL Execution (MySQL)
↓
Retry Mechanism (if failure)
↓
Evaluation + Logging
↓
Dashboard (Power BI)

---

## Tech Stack

| Layer | Technology |
|------|----------|
| Frontend | Streamlit |
| Backend | FastAPI |
| LLM | LLaMA (vLLM GPU / Ollama) |
| Database |
