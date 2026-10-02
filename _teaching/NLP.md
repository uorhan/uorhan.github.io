---
title: "Natural Language Processing"
collection: teaching
type: "Undergraduate Course"
permalink: /teaching/NLP
venue: "CuCEng"
date: 2026-09-15
---

### Course Objectives
The primary objective of this course is to introduce classical Natural Language Processing (NLP) problems and explore their evolution. Students will learn the theoretical foundations of traditional approaches, follow the path from n-gram language models to Transformers, and transition to solving these problems using modern, locally-hosted Large Language Models (LLMs) via the Ollama ecosystem. The course heavily emphasizes engineering practices, strict structured output generation (JSON), evaluating model performance using standard metrics (BLEU, METEOR, chrF, ROUGE), and analyzing model limitations such as hallucinations and context window boundaries.

### Course Materials
- Daniel Jurafsky and James H. Martin, *[Speech and Language Processing](https://web.stanford.edu/~jurafsky/slp3/)* (3rd Edition, latest online draft).
- Official [Ollama Documentation](https://github.com/ollama/ollama) for local LLM deployment.
- [Hugging Face LLM Course](https://huggingface.co/learn/llm-course) and library documentations.

### Assessment
- **40%** Personal Task <!-- TODO: add a short description or a link, e.g. /files/NLP-Personal-Task -->
- **60%** Three Projects and Presentations (20% each) — see the [project descriptions](/files/NLP-Projects)

There is no written midterm or final exam in this course.

### Prerequisites
Basic knowledge of Python programming and Machine Learning fundamentals is strongly recommended.

### Weekly Schedule

| Week | Subjects | Note |
|------|-----------|------|
| 1 | Introduction to NLP & Text Preprocessing: Tokens vs. Words |  |
| 2 | Word Representation: From BoW & TF-IDF to Dense Vectors |  |
| 3 | Language Models: From N-grams to Transformers & Attention |  |
| 4 | Local LLMs (Ollama): Setup, Hardware Limits, Quantization (GGUF) & Generation Parameters |  |
| 5 | Text Classification & Prompt Engineering Fundamentals: Classical ML vs. LLM Prompting |  |
| 6 | Structured Generation: Forcing LLMs to Output JSON |  |
| 7 | Information Extraction: Traditional NER vs. LLM Parsing | **Project I due** |
| 8 | **Midterm Week** — no exam for this course |  |
| 9 | Hallucinations: Confabulation Analysis & Prompt Traps |  |
| 10 | Closed-Domain QA & Groundedness Tests |  |
| 11 | Machine Translation & Paraphrasing: Evaluation (BLEU, METEOR, chrF) |  |
| 12 | Text Summarization: Extractive vs. Abstractive (ROUGE Metrics) | **Project II due** |
| 13 | Processing Large Documents: Chunking & Context Window Limits |  |
| 14 | Open Source Ecosystem: Model Families, Licenses & Benchmarks |  |
| 15 | **Project Presentations** | **Project III due** |

