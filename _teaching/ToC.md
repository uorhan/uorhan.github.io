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

| Week | Subjects |
|------|-----------|
| 1 | Discrete Mathematical Structures review |
| 2 | Deterministic (DFA) and Non-Deterministic (NFA) Finite Automata |
| 3 | NFA to DFA, Regular Expressions (RegEx) |
| 4 | DFA to RegEx, Pumping Lemma for Regular Languages |
| 5 | Context-Free Grammars, Chomsky Normal Form (CNF) |
| 6 | Push-Down Automata (PDA), CNF to PDA |
| 7 | Pumping Lemma for Context-Free Languages |
| 8 | Midterm exam |
| 9 | Turing Machines, Church-Turing Thesis |
| 10 | Non-Deterministic Turing Machines |
| 11 | Decidable and Undecidable Languages |
| 12 | Enumerability and Enumerable Languages |
| 13 | Introduction to Complexity Theory, P & NP classes |
| 14 | Non-Deterministic algorithms, NP-Complete Languages |
| 15 | Review for Final Exam |

## Resources
Below you can find past exam papers.
<p style="line-height: 1.8;">
  {% assign files = site.static_files | where_exp: "file", "file.path contains '/assets/exams/ToC/'" %}
  {% assign pdf_files = files | where_exp: "file", "file.extname == '.pdf'" %}

  {% for file in pdf_files %}
    <a href="{{ file.path | relative_url }}">{{ file.name | downcase }}</a>
    {% unless forloop.last %} | {% endunless %}
  {% endfor %}
</p>

