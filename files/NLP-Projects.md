---
title: "NLP Project Task: 3 Projects"
date: 2026-9-15
---

## Description

This document outlines the three major projects for the Natural Language Processing course. All projects must be implemented using **local open-source LLMs via the Ollama ecosystem** and Python. Cloud APIs (like OpenAI) are strictly forbidden for these tasks. 

Submissions should include a well-documented Jupyter Notebook (or Python scripts) and a brief technical report explaining your methodology and evaluation results.

---

## Project I: Structured Text Classification & Information Extraction

### Objective
To move beyond conversational "black-box" LLM usage by forcing the model to generate strictly structured data that can be programmatically parsed and integrated into software systems.

### Task Description
You will use a local LLM to classify texts and extract specific entities from an unstructured dataset (e.g., IMDB reviews, Turkish news articles, or medical epikrisis reports). 

### Engineering Constraints
* **No Free-Text Allowed:** The model's output must be strictly in a valid JSON format (e.g., `{"category": "sports", "sentiment_score": 0.8, "entities": ["person A", "location B"]}`).
* **Exception Handling:** LLMs often hallucinate or break formatting (e.g., adding markdown blocks like ` ```json ` or conversational text like "Here is your JSON..."). You must write Python code to clean the output, parse the JSON, and include `try-except` blocks to handle parsing failures gracefully.
* **Evaluation:** Calculate and report your JSON parsing success rate (how many prompts resulted in a successfully parsed JSON on the first try) across at least 100 samples.

---

## Project II: Translation, Paraphrasing, and Metric Evaluation

### Objective
To analyze the generative capabilities of LLMs in translation and style transfer, and to scientifically evaluate their output quality using traditional NLP metrics rather than subjective human evaluation.

### Task Description
Select a dataset containing source texts and their reference translations (or paraphrased versions). Instruct the local LLM to translate the text or rewrite it in a different tone (e.g., from informal to academic).

### Engineering Constraints
* **Metric Calculation:** You must computationally evaluate the LLM's outputs against the ground-truth reference texts using **BLEU** and **METEOR** score libraries in Python (e.g., NLTK or Hugging Face `evaluate`).
* **Hyperparameter Analysis:** Run the same task using at least three different `Temperature` values (e.g., 0.1, 0.7, 1.2). 
* **Deliverable:** Plot a graph showing how changing the temperature affects the BLEU/METEOR scores and write a brief analysis discussing the trade-off between determinism and creativity.

---

## Project III: Long Document Summarization & Context Window Management

### Objective
To understand and overcome the hardware limitations and context window boundaries of local Large Language Models when processing large documents.

### Task Description
You are given a long document (e.g., a book chapter, a long research paper, or a financial report) that significantly exceeds the context window (token limit) of your chosen local model. You must design a pipeline to summarize the entire text without losing critical information.

### Engineering Constraints
* **Chunking Strategy:** You must implement a "Map-Reduce" style algorithm. Write Python code to split the document into semantically logical chunks (e.g., by paragraphs or token limits) that fit into the context window.
* **Pipeline Execution:** Summarize each chunk individually (Map phase), and then pass the combined summaries back to the LLM to generate a final master summary (Reduce phase).
* **Evaluation:** Compare your final generated summary against a human-written reference summary using **ROUGE** metrics (ROUGE-1, ROUGE-2, and ROUGE-L). Discuss the "Lost in the Middle" phenomenon and whether your chunking strategy mitigated it.
