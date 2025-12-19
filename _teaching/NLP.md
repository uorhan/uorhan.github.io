---
title: "Natural Language Processing"
collection: teaching
type: "Undergraduate Course"
permalink: /teaching/NLP
venue: "CuCEng"
date: 2025-1-1
---

### Course Objectives
In this course, the main goal is to define the methods and approaches used in Natural Language Processing.

### Course Materials
- Daniel Jurafsky and James H. Martin, *Speech and Language Processing: An Introduction to Natural Language Processing, Computational Linguistics, and Speech*, 2000.

### Assessment
40% Midterm (exam,tasks,etc.) + 60% Final (exam,tasks,etc.)

### Prerequisites
There is no formal prerequisite; however, taking the Theory of Computation (Automata Theory) course beforehand is recommended.

### Weekly Schedule

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
| 15 | Project presentations | <a href="/files/RAG-task">RAG</a> - <a href="/files/LoRa.pdf">LoRA</a> - <a href="/files/Agent.pdf">Agent</a> |

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
