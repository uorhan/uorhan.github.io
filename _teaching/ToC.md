---
title: "Theory of Computation"
collection: teaching
type: "Undergraduate Course"
permalink: /teaching/ToC
venue: "CuCEng"
date: 2025-1-1
---

### Course Objectives
In this course, the main goal is to define the language classes in terms of grammars and automata.

### Course Materials
- Anil Maheshwari and Michiel Smid, *Introduction to Theory of Computation*, Carleton University, 2012.  
- Michael Sipser, *Introduction to the Theory of Computation*, 2nd Edition, Thomson Course Technology, Boston, 2006.  
- John C. Martin, *Introduction to Languages and the Theory of Computation*, 4th Edition, McGraw-Hill, 2011.

### Assessment
40% Midterm (exam,tasks,etc.) + 60% Final (exam,tasks,etc.)

### Prerequisites
There is no formal prerequisite; however, taking the Discrete Mathematics course beforehand is recommended.

### Weekly Schedule

| Week | Subjects | Lesson |
|------|-----------|--------|
| 1 | Discrete Mathematical Structures review |[Lesson 1](/assets/exams/ToC/ToC-1.pdf) | 
| 2 | Deterministic (DFA) and Non-Deterministic (NFA) Finite Automata |[Lesson 2](/assets/exams/ToC/ToC-2.pdf) |
| 3 | NFA to DFA, Regular Expressions (RegEx) |[Lesson 3](/assets/exams/ToC/ToC-3.pdf) |
| 4 | DFA to RegEx, Pumping Lemma for Regular Languages |[Lesson 4](/assets/exams/ToC/ToC-4.pdf) |
| 5 | Context-Free Grammars, Chomsky Normal Form (CNF) |[Lesson 5](/assets/exams/ToC/ToC-5.pdf) |
| 6 | Push-Down Automata (PDA), CNF to PDA |[Lesson 6](/assets/exams/ToC/ToC-6.pdf) |
| 7 | Pumping Lemma for Context-Free Languages |[Lesson 7](/assets/exams/ToC/ToC-7.pdf) |
| 8 | Midterm exam |  |
| 9 | Turing Machines, Church-Turing Thesis |[Lesson 8](/assets/exams/ToC/ToC-8.pdf) |
| 10 | Non-Deterministic Turing Machines |[Lesson 9](/assets/exams/ToC/ToC-9.pdf) |
| 11 | Decidable and Undecidable Languages |[Lesson 10](/assets/exams/ToC/ToC-10.pdf) |
| 12 | Enumerability and Enumerable Languages |[Lesson 11](/assets/exams/ToC/ToC-11.pdf) |
| 13 | Introduction to Complexity Theory, P & NP classes |[Lesson 12](/assets/exams/ToC/ToC-12.pdf) |
| 14 | Non-Deterministic algorithms, NP-Complete Languages |[Lesson 13] |
| 15 | Review for Final Exam |  |

## Resources
Below you can find past exam papers.
<p style="line-height: 1.8;">
  {% assign files = site.static_files | where_exp: "file", "file.path contains '/assets/exams/ToC/'" %}
  {% assign pdf_files = files | where_exp: "file", "file.extname == 'e.pdf'" %}

  {% for file in pdf_files %}
    <a href="{{ file.path | relative_url }}">{{ file.name | downcase }}</a>
    {% unless forloop.last %} | {% endunless %}
  {% endfor %}
</p>

