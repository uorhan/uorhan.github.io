---
title: "Natural Language Processing"
collection: teaching
type: "Undergraduate Course"
permalink: /teaching/NLP
venue: "CuCEng"
date: 2025-1-1
---

### Course Objectives
The primary objective of this course is to introduce classical Natural Language Processing (NLP) problems and explore their evolution. Students will learn the theoretical foundations of traditional approaches and transition to solving these problems using modern, locally-hosted Large Language Models (LLMs) via the Ollama ecosystem. The course heavily emphasizes engineering practices, strict structured output generation (JSON), evaluating model performance using standard statistical metrics (BLEU, ROUGE), and analyzing model limitations such as hallucinations and context window boundaries.

### Course Materials
- Daniel Jurafsky and James H. Martin, *Speech and Language Processing* (3rd Edition Draft), 2024.
- Official [Ollama Documentation](https://github.com/ollama/ollama) for local LLM deployment.
- [Hugging Face NLP Course](https://huggingface.co/learn) and library documentations.

### Assessment
40% (1 Personal Task) + 60% (3 Projects and Presentations)

### Prerequisites
Basic knowledge of Python programming and Machine Learning fundamentals is strongly recommended.

### Weekly Schedule

| Week | Subjects | Note |
|------|-----------|------|
| 1 | Introduction to NLP & Text Preprocessing: Tokens vs. Words | [Lesson 1] |
| 2 | Word Representation: From BoW & TF-IDF to Dense Vectors | [Lesson 2] |
| 3 | Local LLMs (Ollama) Setup & Generation Parameters | [Lesson 3] |
| 4 | Text Classification: Classical ML vs. LLM Prompting | [Lesson 4] |
| 5 | Structured Generation: Forcing LLMs to output JSON | [Lesson 5] |
| 6 | Information Extraction: Traditional NER vs. LLM Parsing | [Lesson 6] |
| 7 | Midterm Review & Prompt Engineering Fundamentals | [Lesson 7] |
| 8 | **Midterm Exam Week** | There is no exam for this course |
| 9 | Hallucinations: Confabulation Analysis & Prompt Traps | [Lesson 8] |
| 10 | Closed-Domain QA & Groundedness Tests | [Lesson 9] |
| 11 | Machine Translation & Paraphrasing: Evaluation (BLEU/METEOR) | [Lesson 10] |
| 12 | Text Summarization: Extractive vs. Abstractive (ROUGE Metrics) | [Lesson 11] |
| 13 | Processing Large Documents: Chunking & Context Window Limits | [Lesson 12] |
| 14 | Open Source Ecosystem, Hardware Limits, & Quantization (GGUF) | [Lesson 13] |
| 15 | **Project Presentations** | <a href="/files/NLP-Projects">1. JSON Parsing - 2. Translation - 3. Summarization</a> |

### OLD Schedule

| Week | Subjects | Note |
|------|-----------|------|
| 1 | Introduction to NLP: Concepts and terms | [Lesson 1](/assets/exams/NLP/NLP1.pdf) |
| 2 | Text Normalization, Lemmatization, Parsing | [Lesson 2](/assets/exams/NLP/NLP2.pdf) |
| 3 | N-Grams and Language Models | [Lesson 3](/assets/exams/NLP/NLP3.pdf) |
| 4 | Corpus (Features and Analysis) | [Lesson 4](/assets/exams/NLP/NLP4.pdf) |
| 5 | Part of Speech Tagging | [Lesson 5](/assets/exams/NLP/NLP5.pdf) |
| 6 | Introduction to Semantic Analysis | [Lesson 6](/assets/exams/NLP/NLP6.pdf) |
| 7 | Ambiguity | [Lesson 7](/assets/exams/NLP/NLP7.pdf) |
| 8 | Midterm Exam |  |
| 9 | Lexical Similarity | [Lesson 8](/assets/exams/NLP/NLP8.pdf) |
| 10 | Semantic Similarity | [Lesson 9](/assets/exams/NLP/NLP9.pdf) |
| 11 | Dialogue Systems, Question Answering | [Lesson 10](/assets/exams/NLP/NLP10.pdf) |
| 12 | Machine Translation | [Lesson 11](/assets/exams/NLP/NLP11.pdf) |
| 13 | Keyword Extraction, Document Summarization | [Lesson 12](/assets/exams/NLP/NLP12.pdf) |
| 14 | Paraphrasing, Ontology Mapping | [Lesson 13](/assets/exams/NLP/NLP13.pdf) |
| 15 | Project presentations | <a href="/files/RAG-task">RAG</a> - <a href="/files/LoRA-task">LoRA</a> - <a href="/files/Agentic-task">Agent</a> |

## Resources
Below you can find past exam papers.
<p style="line-height: 1.8;">
  {% comment %} 1. Önce klasördeki tüm dosyaları al {% endcomment %}
  {% assign folder_files = site.static_files | where_exp: "file", "file.path contains '/assets/exams/NLP/'" %}
  
  {% comment %} 2. Sonra bu dosyalar içinden isminde "-e.pdf" geçenleri süz {% endcomment %}
  {% assign final_files = folder_files | where_exp: "file", "file.name contains '-e.pdf'" %}

  {% for file in final_files %}
    <a href="{{ file.path | relative_url }}">{{ file.name | downcase }}</a>
    {% unless forloop.last %} | {% endunless %}
  {% endfor %}
</p>
