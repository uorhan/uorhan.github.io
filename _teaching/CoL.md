---
title: "Computational Linguistics"
description: Syllabus and reading list for the graduate-level CoL course.
collection: teaching
type: "MSc Course"
permalink: /teaching/CoL
venue: "CuCEng"
date: 2025-1-1
---

## Course Objective 
Theoretical foundations of modern language models, deep linguistic analysis, and LLM architectures. Unlike standard NLP engineering courses, this course focuses on the *"Why"* and *"How"* of linguistic theories as applied to deep learning architectures, moving from sub-word morphology to the latest large language model alignment techniques.

---

## Assessment and Evaluation
- **Paper Critiques (40%):** Weekly critical analysis of the assigned seminal paper (10-12 papers throughout the semester).
- **Applied Term Project (60%):** Literature review, implementation/coding, and final presentation.

---

### Weekly Schedule

| Week | Topic | Seminal Paper (Reading Assignment) |
| :--- | :--- | :--- |
| **1** | **Advanced Morphology & Sub-word Tokenization** | Sennrich, R., et al. (2016). *"Neural Machine Translation of Rare Words with Subword Units".* (BPE Algorithm) |
| **2** | **Syntactic Parsing** | Dozat, T., & Manning, C. D. (2017). *"Deep Biaffine Attention for Neural Dependency Parsing".* |
| **3** | **Distributional & Contextual Semantics** | Peters, M. E., et al. (2018). *"Deep contextualized word representations".* (ELMo) |
| **4** | **Compositional Semantics & Generalization** | Lake, B., & Baroni, M. (2018). *"Generalization without Systematicity: On the Compositional Skills of Seq2Seq Networks".* |
| **5** | **Transformer Architecture & Self-Attention** | Vaswani, A., et al. (2017). *"Attention Is All You Need".* |
| **6** | **LLM Training & PEFT (LoRA)** | Hu, E. J., et al. (2021). *"LoRA: Low-Rank Adaptation of Large Language Models".* |
| **7** | **Alignment & RLHF** | Ouyang, L., et al. (2022). *"Training language models to follow instructions with human feedback".* (InstructGPT) |
| **8** | **RAG & Information Retrieval** | Lewis, P., et al. (2020). *"Retrieval-Augmented Generation for Knowledge-Intensive NLP Tasks".* |
| **9** | **Long Context Management** | Beltagy, I., et al. (2020). *"Longformer: The Long-Document Transformer".* |
| **10** | **Next-Gen Evaluation Metrics** | Zhang, T., et al. (2020). *"BERTScore: Evaluating Text Generation with BERT".* |
| **11** | **Interpretability (XAI) & Probing** | Hewitt, J., & Manning, C. D. (2019). *"A Structural Probe for Finding Syntax in Word Representations".* |
| **12** | **Multilinguality & Low-Resource Languages** | Conneau, A., et al. (2020). *"Unsupervised Cross-lingual Representation Learning at Scale".* (XLM-R) |
| **13** | **Project Presentations - I** | *Literature Review and Methodology Presentation* |
| **14** | **Project Presentations - II** | *Experimental Results and Final Presentation* |

---

### 📝 Paper Reading & Review Template

Students are expected to use the following 4-step template when preparing their weekly paper critiques:

> **1. Problem Identification** > What specific problem are the authors trying to solve? Which gap in the existing literature are they aiming to fill?
>
> **2. Core Innovation (The Hook)** > What is the unique aspect of the proposed method/model? (e.g., Is it a new architecture, a new loss function, or a new dataset?)
>
> **3. Evidence & Experiments** > How did they prove their claims? Which "Baseline" models did they compare against, and on which metrics (SOTA) did they achieve success?
>
> **4. Critique (Weakness)** > What is the missing, biased, or limited aspect of the paper or method that needs future improvement?
