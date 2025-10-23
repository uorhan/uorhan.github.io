---
title: "Introduction to Machine Learning"
collection: teaching
type: "Undergraduate Course"
permalink: /teaching/IML
venue: "CuCEng"
date: 2025-01-01
---

### Course Objectives
Machine Learning is computer algorithms which models the given problem by the data obtained from its media.  
The studies showed the abilities of learning and making decision of machine learning methods are getting important day by day.  
Especially in pattern recognition problems, fast and powerful algorithms are needed.  
In this course, the theoretical and practical foundations of machine learning methods are examined and by these methods, a solution finding to pattern recognition problems is aimed.

### Course Content
Instance-Based Learning; supervised and unsupervised learning; Decision Tree Learning; Bayesian Learning;  
Artificial Neural Networks: feed-forward and feedback paradigms; Assessing, Comparing and Combining Learning Algorithms;  
Feature Extraction and Dimension Reduction; Principal Component Analysis; Linear Discriminant Analysis.

### Course Materials
- T. Mitchell, *Machine Learning*, McGraw-Hill, 1997.  
- C. M. Bishop, *Pattern Recognition and Machine Learning*, Springer, 2007.  
- S. Haykin, *Neural Networks and Learning Machines*, Prentice Hall, 2008.  
- R. O. Duda, *Pattern Classification*, Wiley-Interscience, 2000.  

### Assessment
%40 Midterm (exam,tasks,etc.) + %60 Final (exam,tasks,etc.)

### Prerequisites
It is expected that the students know programming.

### Weekly Schedule


| Week | Topics | Lesson |
|------|---------|--------|
| 1 | Introduction and Basic Concepts of Machine Learning | Lesson 1 |
| 2 | Supervised Learning – Distance Based Classification (K-Nearest Neighbors) | Lesson 2 |
| 3 | Supervised Learning – Probability Based Classification (Naïve Bayes) | Lesson 3 |
| 4 | Supervised Learning – Entropy Based Classification (Decision Trees: ID3, C4.5) | Lesson 4 |
| 5 | Supervised Learning – Lagrange Based Classification (Support Vector Machines) | Lesson 5 |
| 6 | Supervised Learning – Least Squares Based Regression (Ordinary Linear Regression) | Lesson 6 |
| 7 | Unsupervised Learning – Clustering (K-Means) | Lesson 7 |
| 8 | Midterm Exam |  |
| 9 | Unsupervised Learning – Dimensionality Reduction (Principal Component Analysis) | Lesson 8 |
| 10 | Unsupervised Learning – Association Rules (Apriori Algorithm) | Lesson 9 |
| 11 | Reinforcement Learning (Q-Learning) | Lesson 10 |
| 12 | Deep Learning – Perceptron and Adaline | Lesson 11 |
| 13 | Deep Learning – Artificial Neural Networks (MLP and RBF) | Lesson 12 |
| 14 | Deep Learning – Convolutional and Recurrent Neural Networks (CNN and RNN) | Lesson 13 |
| 15 | Deep Learning – Transfer Learning and Transformers | Lesson 14 |
| 16 | Review for Final Exam |  |

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
