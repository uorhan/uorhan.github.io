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
| 1 | Introduction and Basic Concepts of Machine Learning | [Lesson 1](/assets/exams/IML/ML-01.pdf) |
| 2 | Supervised Learning – Distance Based Classification (K-Nearest Neighbors) | [Lesson 2](/assets/exams/IML/ML-02.pdf) |
| 3 | Supervised Learning – Probability Based Classification (Naïve Bayes) | [Lesson 3](/assets/exams/IML/ML-03.pdf) |
| 4 | Supervised Learning – Entropy Based Classification (Decision Trees: ID3, C4.5) | [Lesson 4](/assets/exams/IML/ML-04.pdf) |
| 5 | Supervised Learning – Lagrange Based Classification (Support Vector Machines) | [Lesson 5](/assets/exams/IML/ML-05.pdf) |
| 6 | Supervised Learning – Least Squares Based Regression (Ordinary Linear Regression) | [Lesson 6](/assets/exams/IML/ML-06.pdf) |
| 7 | Unsupervised Learning – Clustering (K-Means) | [Lesson 7](/assets/exams/IML/ML-07.pdf) |
| 8 | Midterm Exam |  |
| 9 | Unsupervised Learning – Dimensionality Reduction (Principal Component Analysis) | [Lesson 8](/assets/exams/IML/ML-08.pdf) |
| 10 | Unsupervised Learning – Association Rules (Apriori Algorithm) | [Lesson 9](/assets/exams/IML/ML-09.pdf) |
| 11 | Reinforcement Learning (Q-Learning) | [Lesson 10] |
| 12 | Deep Learning – Perceptron and Adaline | [Lesson 11] |
| 13 | Deep Learning – Artificial Neural Networks (MLP and RBF) | [Lesson 12] |
| 14 | Deep Learning – Convolutional and Recurrent Neural Networks (CNN and RNN) | [Lesson 13] |
| 15 | Deep Learning – Transfer Learning and Transformers | [Lesson 14] |
| 16 | Review for Final Exam |  |

## Resources
Below you can find past exam papers.
<p style="line-height: 1.8;">
  {% comment %} 1. Önce klasördeki tüm dosyaları al {% endcomment %}
  {% assign folder_files = site.static_files | where_exp: "file", "file.path contains '/assets/exams/IML/'" %}
  
  {% comment %} 2. Sonra bu dosyalar içinden isminde "-e.pdf" geçenleri süz {% endcomment %}
  {% assign final_files = folder_files | where_exp: "file", "file.name contains '-e.pdf'" %}

  {% for file in final_files %}
    <a href="{{ file.path | relative_url }}">{{ file.name | downcase }}</a>
    {% unless forloop.last %} | {% endunless %}
  {% endfor %}
</p>
