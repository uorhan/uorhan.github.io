---
title: "Natural Language Processing"
collection: teaching
type: "Undergraduate Course"
permalink: /teaching/NLP
venue: "CuCEng"
year: 2025-1-1
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
| 1 | Introduction to NLP: Concepts and terms | Lesson 1 |
| 2 | Text Normalization, Lemmatization, Parsing | Lesson 2 |
| 3 | N-Grams and Language Models | Lesson 3 |
| 4 | Corpus (Features and Analysis) | Lesson 4 |
| 5 | Part of Speech Tagging | Lesson 5 |
| 6 | Introduction to Semantic Analysis | Lesson 6 |
| 7 | Ambiguity | Lesson 7 |
| 8 | Midterm Exam |  |
| 9 | Lexical Similarity | Lesson 8 |
| 10 | Semantic Similarity | Lesson 9 |
| 11 | Dialogue Systems, Question Answering | Lesson 10 |
| 12 | Machine Translation | Lesson 11 |
| 13 | Keyword Extraction, Document Summarization | Lesson 12 |
| 14 | Paraphrasing, Ontology Mapping | Lesson 13 |
| 15 | Review for Final Exam |  |

## Resources
Below you can find past exam papers.
<ul>
  {% assign files = site.static_files | where_exp: "file", "file.path contains '/assets/exams/NLP/'" %}
  {% for file in files %}
    {% if file.extname == ".pdf" %}
      <li><a href="{{ file.path | relative_url }}">{{ file.name }}</a></li>
    {% endif %}
  {% endfor %}
</ul>
