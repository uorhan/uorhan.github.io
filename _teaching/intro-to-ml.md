---
title: "Introduction to Machine Learning"
collection: teaching
type: "Undergraduate Course"
permalink: /teaching/intro-to-ml
venue: "CuCEng"
year: 2025-1-1
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

| Week | Subjects | Lesson |
|------|-----------|--------|
| 1 | Instance based Learning, Supervised and Unsupervised Learning | Lesson 1 |
| 2 | K-Means Clustering, Classification by K-Nearest Neighbor | Lesson 2, sample2 |
| 3 | Entropy, Decision Tree Learning, ID3 and C4.5 algorithms, Classification and Regression Trees | Lesson 3, sample3 |
| 4 | Probability and Conditional Probability, Bayesian Theorem, Naive Bayes Classifier, Categorical and Numerical Data | Lesson 4, sample4 |
| 5 | Linear Regression, Multiple Linear Regression, Least Squares Method, Thresholding and Competitive Classification | Lesson 5, sample5 |
| 6 | Fuzzy Logic, Fuzzy Inference Systems | Lesson 6, sample6 |
| 7 | Introduction to Artificial Neural Networks, Perceptron, Adaline, Least Mean Squares | Lesson 7, sample7 |
| 8 | Midterm exam |  |
| 9 | Back-propagation Algorithm, Multi-Layer Perceptron Network | Lesson 8, sample8 |
| 10 | Reinforcement Learning, Q-Learning, TD-Learning, Learning Vector Quantization Network, LVQ2, LVQ-X | Lesson 9, 9-a, 9-b |
| 11 | Mapping and Kernel Functions, Radial Basis Function (RBF), RBF Network | Lesson 10 |
| 12 | Lagrange Method, Optimization by Lagrange Coefficient, Support Vector Machine, Quadratic Programming | Lesson 11 |
| 13 | Feature Extraction and Selection, Dimension Reduction, Principal Component Analysis, Linear Discriminant Analysis | Lesson 12, sample12 |
| 14 | Convolutional and Recurrent Networks, Deep Learning | Lesson 13 |
| 15 | Review for Final Exam |  |

## Resources
Below you can find past exam papers.
<ul>
  {% assign files = site.static_files | where_exp: "file", "file.path contains '/assets/exams/intro-to-ml/'" %}
  {% for file in files %}
    {% if file.extname == ".pdf" %}
      <li><a href="{{ file.path | relative_url }}">{{ file.name }}</a></li>
    {% endif %}
  {% endfor %}
</ul>
