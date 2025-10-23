---
title: "Introduction to Machine Learning"
collection: teaching
type: "Undergraduate Course"
permalink: /teaching/IML
venue: "CuCEng"
date: 2025-01-01
---

### Course Objectives
This course introduces the fundamental principles of machine learning and their real-world applications, enabling students to design and evaluate intelligent systems capable of learning from data.

### Assessment
%40 Midterm (exam,tasks,etc.) + %60 Final (exam,tasks,etc.)

### Prerequisites
It is expected that students have basic programming knowledge (Python or equivalent).

### Weekly Schedule
| Week | Topics | Lesson |
|------|---------|--------|
| 1 | Introduction and Basic Concepts of Machine Learning | [Lesson 1](https://youtube.com/watch?v=example1) |
| 2 | Supervised Learning – Distance Based Classification (K-Nearest Neighbors) | [Lesson 2](https://youtube.com/watch?v=example2) |
| 3 | Supervised Learning – Probability Based Classification (Naïve Bayes) | [Lesson 3](https://youtube.com/watch?v=example3) |
| 4 | Supervised Learning – Entropy Based Classification (Decision Trees: ID3, C4.5) | [Lesson 4](https://youtube.com/watch?v=example4) |
| 5 | Supervised Learning – Lagrange Based Classification (Support Vector Machines) | [Lesson 5](https://youtube.com/watch?v=example5) |
| 6 | Supervised Learning – Least Squares Based Regression (Ordinary Linear Regression) | [Lesson 6](https://youtube.com/watch?v=example6) |
| 7 | Unsupervised Learning – Clustering (K-Means) | [Lesson 7](https://youtube.com/watch?v=example7) |
| 8 | Midterm Exam |  |
| 9 | Unsupervised Learning – Dimensionality Reduction (Principal Component Analysis) | [Lesson 8](https://youtube.com/watch?v=example8) |
| 10 | Unsupervised Learning – Association Rules (Apriori Algorithm) | [Lesson 9](https://youtube.com/watch?v=example9) |
| 11 | Reinforcement Learning (Q-Learning) | [Lesson 10](https://youtube.com/watch?v=example10) |
| 12 | Deep Learning – Perceptron and Adaline | [Lesson 11](https://youtube.com/watch?v=example11) |
| 13 | Deep Learning – Artificial Neural Networks (MLP and RBF) | [Lesson 12](https://youtube.com/watch?v=example12) |
| 14 | Deep Learning – Convolutional and Recurrent Neural Networks (CNN and RNN) | [Lesson 13](https://youtube.com/watch?v=example13) |
| 15 | Deep Learning – Transfer Learning and Transformers | [Lesson 14](https://youtube.com/watch?v=example14) |
| 16 | Review for Final Exam | [Lesson 15](https://youtube.com/watch?v=example15) |

## Resources
Below you can find past exam papers.
<p style="line-height: 1.8;">
  {% assign files = site.static_files | where_exp: "file", "file.path contains '/assets/exams/IML/'" %}
  {% assign pdf_files = files | where_exp: "file", "file.extname == '.pdf'" %}

  {% for file in pdf_files %}
    <a href="{{ file.path | relative_url }}">{{ file.name | downcase }}</a>
    {% unless forloop.last %} | {% endunless %}
  {% endfor %}
</p>
