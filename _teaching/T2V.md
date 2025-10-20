---
title: "Discrete Mathematics"
collection: teaching
type: "Undergraduate Course"
permalink: /teaching/DiM
venue: "CuCEng"
date: 2025-1-1
---

---
title: Text Vectorization (PhD Level)
layout: teaching
permalink: /teaching/T2V
---

## Course Title
**Text Vectorization** Ph.D. (Doctoral Course) - SPRING Semestr

## Course Objective
By the end of this course, students will understand the theoretical foundations behind transforming textual data into numerical representations that can be processed by machine learning models.  
Starting from classical Vector Space Models and TF-IDF, the course explores a wide spectrum of embedding techniques up to modern Transformer-based contextual models. Students will gain both **theoretical insight** and **practical implementation skills**.

---

## Assessment and Evaluation
- **Application Presentation 1:** 20% (Week 5)  
- **Application Presentation 2:** 25% (Week 8)  
- **Application Presentation 3:** 25% (Week 11)  
- **Final Project / Research Paper Presentation:** 30% (Week 15)

---

## 15-Week Intensive Course Schedule

### **Week 1: Introduction and Fundamentals**
- **Topic:** Evolution of text representation. Why vectorization? Basic NLP operations (tokenization, normalization, stemming/lemmatization).  
- **Preparation:** Jurafsky & Martin, *Speech and Language Processing* (Chapters on Regular Expressions, Text Normalization).  
- **Method:** Lecture, Q&A, Discussion.

---

### **Week 2: Frequency-Based Models**
- **Topic:** Bag-of-Words, One-hot vectors, Vector Space Model (VSM), cosine similarity.  
- **Preparation:** Manning, Raghavan & Schütze, *Introduction to Information Retrieval* (Ch. 6).  
- **Method:** Lecture, Mathematical formulation.

---

### **Week 3: Weighting and Dimensionality**
- **Topic:** TF-IDF, Sparsity problem, term specificity, and introduction to PCA/SVD for dimensionality reduction.  
- **Preparation:** Sparck Jones (1972), *A Statistical Interpretation of Term Specificity...*  
- **Method:** Lecture, hands-on examples.  
- **Assignment:** Build a simple search engine using TF-IDF and cosine similarity.

---

### **Week 4: Distributional Semantics**
- **Topic:** Distributional Hypothesis (“You shall know a word by the company it keeps”). Word2Vec architectures: CBOW & Skip-Gram.  
- **Preparation:** Mikolov et al. (2013), *Efficient Estimation of Word Representations in Vector Space.*  
- **Method:** Lecture, architecture illustration.

---

### **Week 5: Application Presentation 1 — Classical Models**
- **Scope:** Classical and statistical representations (BoW, TF-IDF, and VSM).  
- **Task:** Each student presents an implementation project (e.g., document retrieval, similarity analysis, or keyword extraction).  
- **Evaluation:** Methodology (40%), Results (40%), Presentation clarity (20%).  
- **Method:** Student presentations and peer feedback.

---

### **Week 6: Supervised Embedding Models — The SemSpace Approach**
- **Topic:** Supervised data in embedding learning; **Generalized SemSpace** methodology for context- and class-aware representation learning.  
- **Focus:** Using labeled data to construct semantic vector spaces beyond unsupervised Word2Vec/GloVe.  
- **Preparation:** Orhan, U. (2023), *Generalized SemSpace: Supervised Contextual Embedding Model.*  
- **Method:** Lecture, mathematical formulation, and small demonstration.

---

### **Week 7: Sentence Embeddings — ELMo and Contextualized SemSpace**
- **Topic:**  
  - BiLSTM-based contextual embeddings (ELMo)  
  - Contextualized SemSpace (sentence-level supervised contextual model)  
  - Transition from word-level to sentence-level representations  
- **Preparation:** Peters et al. (2018), *Deep Contextualized Word Representations*; Orhan, U. (2024), *Contextualized SemSpace: A Hybrid Contextual Embedding Approach.*  
- **Method:** Lecture, comparative analysis, architecture visualization.

---

### **Week 8: Application Presentation 2 — ELMo-based Contextual Embeddings**
- **Scope:** Hands-on exploration of **ELMo embeddings** and contextualization performance.  
- **Task:** Train or use pre-trained ELMo embeddings on a small dataset (semantic similarity, NER, or sentiment classification).  
- **Deliverables:** Short demo notebook, metrics comparison, and findings on contextual understanding.  
- **Method:** Student presentations and Q&A.  
- **Note:** No midterm exam (replaced by presentations).

---

### **Week 9: Transformer Revolution**
- **Topic:** From sequence models (RNN/LSTM) to Attention and Self-Attention mechanisms; Transformer encoder-decoder structure.  
- **Preparation:** Vaswani et al. (2017), *Attention Is All You Need.*  
- **Method:** Lecture, architecture visualization, discussion.

---

### **Week 10: Contextual Models — BERT Foundations**
- **Topic:** BERT architecture, pre-training objectives (MLM and NSP), embedding structure, and fine-tuning concept.  
- **Preparation:** Devlin
