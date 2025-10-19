---
title: "Discrete Mathematics"
collection: teaching
type: "Undergraduate Course"
permalink: /teaching/DiM
venue: "CuCEng"
date: 2025-1-1
---

## Course Objectives
This course introduces the **mathematical foundations of computer science**, covering topics such as **formal logic**, **set theory**, **mathematical induction**, **methods of counting**, **discrete probability**, and **elementary graph theory**.

## Course Materials
- *Notes on Discrete Mathematics*, M. A. Lerma, Northwestern University  
- *Discrete Mathematical Structures: Theory and Applications*, D. S. Malik and M. K. Sen, Thomson  

## Assessment
- **40%** Midterm (exam, tasks, etc.)  
- **60%** Final (exam, tasks, etc.)

## Prerequisites
None

## Weekly Schedule

| Week | Subjects | Lecture Notes |
|------|-----------|---------------|
| 1 | Introduction to the Course, Logic and Proofs, Propositions | Intro slide, Chapter 1 |
| 2 | Binary Relations, POSet, Hasse Diagram, Equivalent Relation | Chapter 2 |
| 3 | Algorithm Complexity, Modular Arithmetic, RSA | Chapter 3 |
| 4 | Induction & Recurrence, Combinatorics & The Pigeonhole Principle | Chapters 4 & 5 |
| 5 | Probability & Bayes Theorem, Graphs & Representations | Chapters 6 & 7 |
| 6 | Euler Paths/Circuits, Hamilton Paths/Circuits | Chapter 7 |
| 7 | Dijkstra’s Shortest Path, Homeomorphism, Graph Coloring | Chapter 7 |
| 8 | **Midterm Exam** | — |
| 9 | Trees, Binary Trees, Decision Trees, Complexity of Tree Algorithms | Chapter 8 |
| 10 | Tree Isomorphism, Huffman Code, Game Trees & Pruning | Chapter 8 |
| 11 | Transversal Algorithms, Spanning Tree Algorithms | Chapter 8 |
| 12 | Boolean Algebras, Finite-State Machines & Automata | Chapters 9 & 10 |
| 13 | Context-Free Languages & Grammars | Chapter 10 |
| 14 | Regular Expressions & Nondeterministic Finite-State Automata | Chapter 10 |
| 15 | Review for Final Exam | Chapters 1–10 |
| — | **Final Exam** | — |

## Resources
Below you can find past exam papers.
<p style="line-height: 1.8;">
  {% assign files = site.static_files | where_exp: "file", "file.path contains '/assets/exams/DiM/'" %}
  {% assign pdf_files = files | where_exp: "file", "file.extname == '.pdf'" %}

  {% for file in pdf_files %}
    <a href="{{ file.path | relative_url }}">{{ file.name | downcase }}</a>
    {% unless forloop.last %} | {% endunless %}
  {% endfor %}
</p>
