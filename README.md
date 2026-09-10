# 🧬 Bio-Sync

### AI-Powered Multi-Agent Laboratory Test Case Analysis & Report Generation

![Python](https://img.shields.io/badge/Python-3.10+-blue)
![Google Colab](https://img.shields.io/badge/Google%20Colab-Supported-orange)
![LangChain](https://img.shields.io/badge/LangChain-Used-green)
![RAG](https://img.shields.io/badge/RAG-Enabled-purple)
![ChromaDB](https://img.shields.io/badge/ChromaDB-Vector%20DB-red)

## 📌 About

**Bio-Sync** is an AI-powered laboratory test case analysis system that uses **Multi-Agent AI, LLMs, RAG, and ChromaDB** to automatically analyze biological test cases and generate structured reports.

The system accepts test cases written in natural language and identifies whether biological measurements are **NORMAL** or **ANOMALY** based on predefined laboratory baselines.

## 🤖 Multi-Agent System

The project uses three AI agents:

- 🔵 **Ingestor Agent** – Extracts test case and biological measurements.
- 🟢 **Analyst Agent** – Compares measurements with biological baselines using RAG.
- 🟣 **Summarizer Agent** – Generates the final laboratory report.

## 🔎 RAG Pipeline

```text
Baseline Document
       ↓
Text Splitting
       ↓
HuggingFace Embeddings
       ↓
ChromaDB
       ↓
Relevant Baseline Retrieval
       ↓
Analyst Agent
```
## 🧬 Biological Baselines

| Measurement | Normal Range |
|---|---|
| ❤️ Heart Rate | **500–700 bpm** |
| 🌡️ Body Temperature | **36.5–38.0 °C** |
| 🫁 Respiratory Rate | **80–200 breaths/min** |

**Values outside these ranges are marked as ANOMALY.**

## ✨ Features

- 🤖 **Multi-Agent AI Architecture**
- 🔎 **Retrieval-Augmented Generation (RAG)**
- 🧠 **Large Language Model Integration**
- 📚 **ChromaDB Vector Database**
- 🔤 **HuggingFace Embeddings**
- 📝 **Natural Language Test Case Input**
- 🚨 **Automatic Anomaly Detection**
- 📄 **Automated Report Generation**
- ☁️ **Google Colab Based**

## 🛠️ Technologies

- **Python**
- **LangChain**
- **OpenRouter**
- **ChromaDB**
- **HuggingFace Sentence Transformers**
- **IPyWidgets**
- **Google Colab**

## 🎓 Academic Purpose

This project demonstrates practical applications of:

- **Artificial Intelligence**
- **Generative AI**
- **Multi-Agent Systems**
- **RAG**
- **LLMs**
- **Vector Databases**
- **Natural Language Processing**

## 👩‍💻 Author

**Sakshi Sambherao**

## 🧬 Bio-Sync

### **AI-Powered Multi-Agent Laboratory Test Case Analysis & Report Generation**
