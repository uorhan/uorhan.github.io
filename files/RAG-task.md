---
title: "NLP Project Task: Sectoral RAG System Optimization"
date: 2025-1-1
categories: [NLP, Project, RAG, AI]
tags: [rag, llm, chunking, vector-db]
description: "A task to transform a static LLM into a RAG system capable of hybrid search by feeding it sectoral documents, and to optimize it."
---

In this project, you will transform a static Language Model (LLM) that produces fixed responses into a **RAG (Retrieval-Augmented Generation)** system that generates answers by retrieving information from external sources (PDF documents), and you will optimize this system according to your chosen sector.

## 📚 Prerequisites: What is RAG?

Before starting the project, you need to review the following resources:

* **Project Guide:** [RAG System and Optimization Guide (PDF)](https://uorhan.github.io/files/rag.pdf)
* **Reference Code:** [RAG Academic Assistant Repository](https://github.com/naholav/rag-academic-assistant)

**Brief Summary:**
[cite_start]RAG systems are used to solve the "hallucination" (fabrication) problem of LLMs and to provide the model with up-to-date/private information [cite: 31-32]. Success in this architecture depends on how the text is divided (**Chunking**), how it is searched (**Hybrid Search**), and how creative the model is allowed to be (**Temperature**).

---

## 🎯 Task Steps

### Step 1: Sector and Data Selection
Determine a specialized field for yourself (e.g., Law, Medicine, Finance, Engineering Standards, Game Rules, etc.).
* [cite_start]Find **at least 2 technical PDF documents** related to this field [cite: 319-320].
* *Goal:* To test your system not with general culture questions ("What is the capital of France?"), but with specific information found only in those documents.

### Step 2: Installation
Clone the reference project to your computer (or Colab/Cloud environment) and install it:

```bash
git clone [https://github.com/naholav/rag-academic-assistant](https://github.com/naholav/rag-academic-assistant)
cd rag-academic-assistant
pip install -r requirements.txt
Note: The system uses the ChromaDB vector database and the Qwen model by default.

### Step 3: Experimental Optimization (Critical Stage)
Using the "Interactive Parameter Exploration" section in the guide document as a reference, you must find the best settings for your own data. You are required to conduct the following 3 experiments and report the results:

### 🧪 Experiment A: Chunking Strategy

Test which size works better by dividing your texts into different sizes:

Small Chunk (200-400 tokens): For precise definitions and short answers.

Large Chunk (1000+ tokens): For complex topics requiring broad context.

Optimal: Generally, 800 tokens and 150 overlap are recommended; what is the situation with your data? .


### 🔍 Experiment B: Search Method (Hybrid Search)

Identify a question containing technical terms specific to your sector (e.g., "What is the performance of OCR-Qwen-32B?").

Semantic Only (Weight 1.0): Performs meaning-based search.

Keyword Only (Weight 1.0 - BM25): Performs exact word matching.

Hybrid (Recommended): 70% Semantic + 30% Keyword. Which method found the correct page?

### 🤖 Experiment C: Accuracy Test (RAG vs Pure LLM)

Ask the model for a very specific piece of information found in your document.

Scenario 1 (Pure LLM): The model's answer when RAG is off (Usually "I don't know" or a hallucinated answer) .

Scenario 2 (RAG): The answer provided when RAG is on, including citations .

---

## 📦 Deliverables

At the end of the project, you must prepare the following content:

### GitHub Repository:

The PDF files you used.
The working version of the project (if you made changes to the code).

### Project Report (PDF):

Sector Definition: Which field did you choose?
Parameter Table: The best settings you found for your data (Chunk Size, Overlap, Temperature, etc.).
Evidence: Screenshots of the Q&A sessions obtained from Experiments A, B, and C.

## 💡 Tips and Troubleshooting

Hardware: The code uses CUDA (GPU) by default. If you do not have a GPU, change the device setting to cpu, but answer generation may slow down.

OOM (Out of Memory): If you get a memory error:

Reduce the Chunk Size (e.g., 500).

Decrease the Candidates to Retrieve count (e.g., 10 instead of 20).

Temperature Setting: Temperature: 0.3 (More consistent) is recommended for technical documents. You can increase this value for creative writing tasks.
