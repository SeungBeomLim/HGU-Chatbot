# Development of a Handong University Chatbot Using LLMs

This project proposes a methodology to build a domain-specific small language model (sLLM) chatbot that can understand and answer questions based on internal university policy documents, such as academic regulations and scholarship notices.

By avoiding the use of commercial APIs or frameworks like LangChain or OpenAI, this project demonstrates how to design and implement a fully self-hosted and secure RAG-like chatbot system from scratch.

---

## 🧠 Project Overview

- **Objective**: Build an LLM-based chatbot that delivers accurate, reliable answers grounded in Handong University’s internal documents
- **Architecture**: Custom-built RAG-style pipeline without external dependencies
- **Security Focus**: No data is sent outside; suitable for on-premise environments

---

## 🖼 Architecture

> _Full pipeline from document ingestion to generation, including retrieval and final response._

![Chatbot Architecture]
<img width="820" alt="Image" src="https://github.com/user-attachments/assets/e9ccc096-18f7-47da-813c-6bdb7502b294" />

---

## ⚙️ Tech Stack

| Component           | Tools / Libraries                    |
|---------------------|--------------------------------------|
| Language            | Python                               |
| Embedding Model     | KURE-v1                              |
| Vector DB           | MongoDB                              |
| Retriever           | Custom retriever logic (fine-tuned)  |
| Generator           | Llama-3.2-Korean-Bllossom-AICA-5B    |
| Verification        | BertScore(F1), Domain Expert         |
| Interface           | Streamlit                            |

---

## 🔍 Key Features

- Full custom RAG pipeline with no external framework dependency
- Document chunking, preprocessing, and structured DB construction
- Top-3 retrieval accuracy over 97.77%
- Dynamic prompt engineering tailored for each data type
- Self-check module for generation reliability

---

## ⚠️ Challenges & Solutions

### 1. Data inconsistencies and noise made it difficult to create clean inputs for fine-tuning and retrieval
Applied a two-stage preprocessing pipeline and combined automated and manual cleanup strategies

### 2.  Initial retrieval accuracy did not meet our 95% Top-3 target
Refined datasets, fine-tuned retriever models, and achieved 97.77% Top-3 accuracy

### 3. sLLM generation quality was unstable and inconsistent in Korean
Used a Korean fine-tuned LLaMA model with additional tuning and prompt optimization for reliable outputs

---

## 📂 Repository Info

> This repository was created post-project for documentation purposes.  
> Currently under active development.  
> **Private Repository** – https://github.com/justin-tak0426/Handong-Global-University-sLLM_Chatbot

---

## ✍️ Author Info

**Team**: Luminis - Machine Intelligence Lab (MILAB) 
**Project Type**: Capstone + Research (KCC 2025 Submission)

