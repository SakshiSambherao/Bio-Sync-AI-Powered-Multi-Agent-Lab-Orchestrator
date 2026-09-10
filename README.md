# 🧬 Bio-Sync
### AI-Powered Multi-Agent Laboratory Test Case Analysis & Report Generation

<p align="center">

![Python](https://img.shields.io/badge/Python-3.10%2B-blue?logo=python)
![Google Colab](https://img.shields.io/badge/Google%20Colab-Notebook-orange?logo=googlecolab)
![LangChain](https://img.shields.io/badge/LangChain-Framework-green)
![ChromaDB](https://img.shields.io/badge/ChromaDB-Vector%20Database-purple)
![RAG](https://img.shields.io/badge/RAG-Retrieval%20Augmented%20Generation-red)
![OpenRouter](https://img.shields.io/badge/OpenRouter-LLM-black)
![Status](https://img.shields.io/badge/Status-Active-success)

</p>

---

## 📌 Project Overview

**Bio-Sync** is an AI-powered **Multi-Agent Laboratory Test Case Analysis and Report Generation System**.

The system allows users to enter a laboratory test case in **natural language or unstructured/random wording** through a single input box.

The system automatically:

- Extracts laboratory information
- Retrieves biological baseline information
- Analyzes biological measurements
- Identifies normal and abnormal values
- Generates a professional laboratory test case report

The project combines **Large Language Models (LLMs), Multi-Agent AI, Retrieval-Augmented Generation (RAG), and ChromaDB** into a single workflow.

---

## 🎯 Objectives

The main objectives of Bio-Sync are:

1. To accept laboratory test cases using natural language.
2. To automatically extract important biological measurements.
3. To retrieve relevant baseline information using RAG.
4. To compare measurements with predefined biological ranges.
5. To identify normal and abnormal measurements.
6. To generate a structured laboratory report automatically.
7. To demonstrate the use of multiple specialized AI agents.
8. To provide a simple Google Colab-based interface.

---

# 🏗️ System Architecture

```text
                         ┌──────────────────────┐
                         │       USER           │
                         │  Laboratory Test Case│
                         └──────────┬───────────┘
                                    │
                                    ▼
                         ┌──────────────────────┐
                         │   INGESTOR AGENT     │
                         │                      │
                         │ Extracts:            │
                         │ • Test Case ID       │
                         │ • Subject ID         │
                         │ • Heart Rate         │
                         │ • Temperature        │
                         │ • Respiratory Rate   │
                         └──────────┬───────────┘
                                    │
                                    ▼
                         ┌──────────────────────┐
                         │    ANALYST AGENT     │
                         │                      │
                         │ Compares measurements│
                         │ with biological      │
                         │ baseline ranges      │
                         └──────────┬───────────┘
                                    │
                                    │
                         ┌──────────▼───────────┐
                         │       RAG SYSTEM     │
                         │                      │
                         │     ChromaDB         │
                         │          +           │
                         │ HuggingFace Embeddings│
                         └──────────┬───────────┘
                                    │
                         Biological Baselines
                                    │
                                    ▼
                         ┌──────────────────────┐
                         │  ANALYSIS RESULTS    │
                         │                      │
                         │ NORMAL / ANOMALY     │
                         └──────────┬───────────┘
                                    │
                                    ▼
                         ┌──────────────────────┐
                         │  SUMMARIZER AGENT    │
                         │                      │
                         │ Creates professional │
                         │ laboratory report    │
                         └──────────┬───────────┘
                                    │
                                    ▼
                         ┌──────────────────────┐
                         │    FINAL REPORT      │
                         │                      │
                         │ Test Case Analysis   │
                         │ Summary & Follow-up  │
                         └──────────────────────┘
🤖 Multi-Agent Workflow

Bio-Sync uses three specialized AI agents.

🔵 1. Ingestor Agent

Responsible for extracting information from the user's test case.

Input:

TC001 Mouse 001 has heart rate 750 bpm,
temperature 37.2 C and respiratory rate 90 bpm.

Output:

Test Case ID: TC001
Subject ID: Mouse 001
Heart Rate: 750 bpm
Body Temperature: 37.2 C
Respiratory Rate: 90 bpm
🟢 2. Analyst Agent

The Analyst Agent:

Retrieves biological baseline information using RAG.
Compares actual measurements with normal ranges.
Determines whether each value is NORMAL or ANOMALY.
Provides a reason for abnormal values.
🟣 3. Summarizer Agent

The Summarizer Agent converts the analysis into a structured report containing:

Test Case Information
Overall Result
Measurement Analysis
Abnormal Measurements
Normal Measurements
Executive Summary
Recommended Follow-up
🔎 Retrieval-Augmented Generation (RAG)

Bio-Sync uses RAG to retrieve the biological baseline information before performing the analysis.

RAG Pipeline
Biological Baseline Document
            │
            ▼
      Text Splitting
            │
            ▼
   HuggingFace Embeddings
            │
            ▼
         ChromaDB
            │
            ▼
        Retriever
            │
            ▼
     Relevant Baseline
            │
            ▼
      Analyst Agent
🧪 Biological Baselines

The current system uses the following baseline ranges:

Measurement	Normal Range	Unit
❤️ Heart Rate	500 – 700	bpm
🌡️ Body Temperature	36.5 – 38.0	°C
🫁 Respiratory Rate	80 – 200	breaths/min

Values outside these ranges are flagged as ANOMALY.

Note: These baseline values are project/demo data and are not intended for clinical diagnosis.

✨ Features
Feature	Description
🤖 Multi-Agent AI	Uses specialized agents for ingestion, analysis and reporting
📝 Natural Language Input	Accepts structured or unstructured test cases
🔎 RAG	Retrieves relevant biological baseline information
🗄️ ChromaDB	Stores and retrieves document embeddings
🧠 LLM	Uses OpenRouter-compatible language models
📊 Anomaly Detection	Identifies measurements outside baseline ranges
📄 Automatic Reports	Generates professional test case reports
🚫 No Data Fabrication	Missing measurements are not invented
💻 Google Colab	Runs directly in Google Colab
🎯 Single Input Box	Simple user interface
🔐 Secure API Key	Uses Google Colab Secrets
⚡ Automated Workflow	Test case to final report automatically
🛠️ Technologies Used
Programming Language
🐍 Python
AI / LLM
Large Language Models
OpenRouter API
LangChain
Multi-Agent System
Ingestor Agent
Analyst Agent
Summarizer Agent
RAG
Retrieval-Augmented Generation
HuggingFace Sentence Transformers
ChromaDB
Interface
IPyWidgets
Google Colab
📦 Project Structure
Bio-Sync/
│
├── 📓 Bio_Sync.ipynb
│
├── 📄 baselines.txt
│
└── 📖 README.md
Files
File	Description
Bio_Sync.ipynb	Complete Google Colab implementation
baselines.txt	Biological baseline knowledge used by RAG
README.md	Project documentation
🚀 Installation & Setup
1️⃣ Open Google Colab

Open the Bio_Sync.ipynb notebook in Google Colab.

2️⃣ Install Dependencies

Run:

!pip install -q langchain langchain-openai langchain-community langchain-chroma langchain-huggingface langchain-text-splitters sentence-transformers chromadb ipywidgets
3️⃣ Configure OpenRouter API Key

Store your OpenRouter API key in Google Colab Secrets.

Use the secret name:

GenAi_Chatbot

The notebook retrieves the key securely:

from google.colab import userdata

OPENROUTER_API_KEY = userdata.get("GenAi_Chatbot")

⚠️ Never upload your API key to GitHub.

4️⃣ Run the Notebook

Run the notebook cells in order.

The system will:

Load Baselines
      ↓
Create Embeddings
      ↓
Create ChromaDB
      ↓
Initialize LLM
      ↓
Initialize Agents
      ↓
Create Input Interface
      ↓
Generate Report
🧪 Example Test Cases
Example 1 — Mixed Results
Input
TC001 Mouse 001: Heart Rate 750 bpm,
Temperature 37.2 C,
Respiratory Rate 90 breaths/min.
Expected Analysis
Heart Rate: ANOMALY
Temperature: NORMAL
Respiratory Rate: NORMAL
Example 2 — Temperature Anomaly
Input
Test Case TC002.
Mouse 002 has a heart rate of 600 bpm,
temperature of 39.5 C and breathing rate
of 120 breaths per minute.
Expected Analysis
Heart Rate: NORMAL
Temperature: ANOMALY
Respiratory Rate: NORMAL
Example 3 — Natural / Random Wording
Input
Mouse 014 was checked today. The heart was
beating around 480 bpm, temperature was 38.7
degrees and breathing was nearly 150 per minute.
Case ID TC014.

The Ingestor Agent extracts the information even though the input does not follow a fixed format.

Expected Analysis
Heart Rate: ANOMALY
Temperature: ANOMALY
Respiratory Rate: NORMAL
Example 4 — Missing Measurement
Input
TC005 Mouse 005 has a heart rate of 800 bpm
and temperature of 37.5 C.

The system should not invent the respiratory rate.

Heart Rate: ANOMALY
Temperature: NORMAL
Respiratory Rate: Not Provided

📊 System Workflow
        ┌─────────────────┐
        │   User Input    │
        └────────┬────────┘
                 │
                 ▼
        ┌─────────────────┐
        │ Ingestor Agent  │
        └────────┬────────┘
                 │
                 ▼
        ┌─────────────────┐
        │ Extracted Data  │
        └────────┬────────┘
                 │
                 ▼
        ┌─────────────────┐
        │  Analyst Agent  │
        └────────┬────────┘
                 │
                 ▼
        ┌─────────────────┐
        │ RAG + ChromaDB  │
        └────────┬────────┘
                 │
                 ▼
        ┌─────────────────┐
        │ Normal/Anomaly  │
        │    Analysis     │
        └────────┬────────┘
                 │
                 ▼
        ┌─────────────────┐
        │Summarizer Agent │
        └────────┬────────┘
                 │
                 ▼
        ┌─────────────────┐
        │  Final Report   │
        └─────────────────┘

🎓 Academic Applications

This project demonstrates concepts from:

Artificial Intelligence
Generative AI
Large Language Models
Multi-Agent Systems
Natural Language Processing
Retrieval-Augmented Generation
Vector Databases
Information Extraction
Automated Report Generation
🔮 Future Enhancements

Future versions of Bio-Sync can include:

📄 PDF report generation
📊 Graphical measurement visualization
📁 CSV/Excel test case upload
🗃️ Database storage for previous reports
📈 Historical measurement tracking
🧪 Additional biological parameters
🤖 More specialized AI agents
📧 Automated report sharing
🔍 Advanced anomaly detection
🌐 Web-based interface
📱 Mobile application
📥 Downloadable reports
⚠️ Disclaimer

Bio-Sync is an educational and demonstration project.

The biological baseline values used in this project are provided as project/demo data. The generated reports are intended for laboratory test-case analysis and must not be interpreted as medical diagnoses or professional medical advice.

👩‍💻 Author
Sakshi Sambherao – 109

🎓 AI / Generative AI Project

⭐ Conclusion

Bio-Sync demonstrates how Multi-Agent AI, Large Language Models, RAG, embeddings, and vector databases can work together to transform an unstructured laboratory test case into a structured analysis report.

The system simplifies the complete workflow:

Input
  ↓
Extract
  ↓
Retrieve
  ↓
Analyze
  ↓
Summarize
  ↓
Report
<p align="center">
🧬 Bio-Sync

From Laboratory Test Case to Intelligent Report

⭐ Star this repository if you find it useful!

</p> ```
