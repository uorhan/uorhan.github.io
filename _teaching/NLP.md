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
There is no written midterm or final exam in this course. Grades are based on two components:

- **40%** – Presentation Task: Every student must present at least one course topic in class. Topics are taken in class on a volunteer basis, so you must attend the lectures to take a topic. After your presentation, upload your slides through the [upload form](https://forms.gle/KY55TRWjmc3bHwm48). If an additional task is given, upload the extended version again through the same form. A student who does not present any topic by the end of the semester receives zero for this component.
- **60%** – Three Projects (20% each): Each project is presented by video (see the [project descriptions](/files/NLP-Projects)). In Week 15, every student takes an in-person **final oral exam** covering all defense questions of Projects I, II and III, not only the ones answered in the videos. The project grades are given after the oral exam. A student who does not attend the oral exam receives zero for all three projects.

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
| 7 | Information Extraction: Traditional NER vs. LLM Parsing | |
| 8 | **Midterm Week** — no exam for this course |  |
| 9 | Hallucinations: Confabulation Analysis & Prompt Traps |  |
| 10 | Closed-Domain QA & Groundedness Tests | [**Project I due**](/files/NLP-Project-1) |
| 11 | Machine Translation & Paraphrasing: Evaluation (BLEU, METEOR, chrF) |  |
| 12 | Text Summarization: Extractive vs. Abstractive (ROUGE Metrics) | [**Project II due**](/files/NLP-Project-2) |
| 13 | Processing Large Documents: Chunking & Context Window Limits |  |
| 14 | Open Source Ecosystem: Model Families, Licenses & Benchmarks |  [**Project III due**](/files/NLP-Project-3) |
| 15 | **Final Oral Exam** (in person): all defense questions of Projects I–III | [Descriptions of the projects](/files/NLP-Projects) |

