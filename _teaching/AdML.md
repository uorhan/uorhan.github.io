---
title: "Advanced Machine Learning"
description: Syllabus and reading list for the graduate-level AdML course.
collection: teaching
type: "MSc Course"
permalink: /teaching/adML
venue: "CuCEng"
date: 2025-1-1
---

## Course Description
This Master's level course dives deep into the theoretical and practical foundations of modern machine learning, focusing primarily on Deep Learning (DL) architectures, advanced optimization techniques, and probabilistic models. The course adopts a **seminar and project-based** structure, requiring students to engage critically with seminal papers and implement sophisticated models.

Students will be assessed solely based on weekly critiques and a significant hands-on term project.

---

## Assessment and Evaluation

| Component | Weight | Description |
| :--- | :--- | :--- |
| **Weekly Paper Critique & Participation** | **40%** | Critical analysis of the assigned reading and active engagement in discussion. |
| **Final Project** | **60%** | Code implementation, technical report, and final presentation.

---

## Weekly Schedule and Reading List

The curriculum is structured around three modules: **Deep Foundations**, **Architectures & Generative Models**, and **Special Topics**.

| Week | Topic | Primary Reading (Paper/Chapter) |
| :--- | :--- | :--- |
| **1** | **Foundations & Advanced Optimization** <br> (Review of SGD, Momentum, Adam) | **Book Chapter:** Goodfellow et al. *Deep Learning*, Chapter 8 (Optimization). |
| **2** | **Regularization in DL** <br> (Batch Normalization, Dropout, L2) | **Paper:** Ioffe, S., & Szegedy, C. (2015). *Batch Normalization: Accelerating Deep Network Training*. ICML. |
| **3** | **Probabilistic ML & GPs** <br> (Gaussian Processes, Bayesian Inference) | **Book Chapter:** Bishop, C. M. *PRML*, Chapter 2 & 6 (Gaussian Processes). |
| **4** | **Convolutional Architectures** <br> (ResNets, VGG, Modern CNNs) | **Paper:** He, K. et al. (2016). *Deep Residual Learning for Image Recognition*. CVPR. |
| **5** | **Sequence Modeling with RNNs** <br> (LSTMs, GRUs, Backpropagation Through Time) | **Paper:** Hochreiter, S., & Schmidhuber, J. (1997). *Long Short-Term Memory*. Neural Computation. |
| **6** | **Attention Mechanisms** <br> (Soft Attention, Global/Local Attention) | **Paper:** Bahdanau, D. et al. (2015). *Neural Machine Translation by Jointly Learning to Align and Translate*. ICLR. |
| **7** | **The Transformer Model** <br> (Architecture, Positional Encoding, Multi-head Attention) | **Seminal Paper:** Vaswani, A. et al. (2017). *Attention Is All You Need*. NeurIPS. |
| **8** | **Midterm Week / No Exam - No Class** |
| **9** | **Variational Autoencoders (VAEs)** <br> (ELBO, Latent Space Sampling) | **Paper:** Kingma, D. P., & Welling, M. (2014). *Auto-Encoding Variational Bayes*. ICLR. |
| **10** | **Generative Adversarial Networks (GANs)** <br> (Minimax Game, WGANs, Training Stability) | **Paper:** Goodfellow, I. et al. (2014). *Generative Adversarial Networks*. NeurIPS. |
| **11** | **Transfer Learning & Fine-Tuning** <br> (Pre-trained Models: BERT, ViT, Adapter Layers) | **Paper:** Devlin, J. et al. (2019). *BERT: Pre-training of Deep Bidirectional Transformers for Language Understanding*. NAACL. |
| **12** | **Reinforcement Learning & Constitutional AI** <br> (RLHF, Value Alignment, Ethical Control) | **Paper:** Bai, Y. et al. (2022). *Constitutional AI: Harmlessness from AI Feedback*. arXiv. |
| **13** | **Explainable AI (XAI) & Ethics** <br> (LIME, SHAP, Interpretability vs. Explainability) | **Survey Paper:** Lipton, Z. (2018). *The Mythos of Model Interpretability*. ML for Healthcare. |
| **14** | **Final Project Presentations** | *Demonstration of working models and presentation of the final research findings.* |

---

## Term Project Topics

Students are required to select one topic and deliver a **functional codebase, a technical report, and a final presentation**. The projects must involve the implementation or fine-tuning of an advanced ML architecture.

### 1. Transformer Implementation for Time Series Forecasting
**Goal:** Implement the Transformer architecture (or a specialized variant like Informer/Autoformer) from scratch and apply it to a multivariate time series forecasting task (e.g., energy consumption or stock prices).
* **Focus:** Attention mechanism visualization and complexity analysis.

### 2. Controllable Image Generation using VAEs/GANs
**Goal:** Implement a VAE or a conditional GAN (cGAN) and train it on a specific dataset (e.g., CelebA for faces or a custom dataset).
* **Focus:** Manipulate the latent space to control a specific output feature (e.g., generating images with specific attributes).

### 3. Deep Reinforcement Learning for Simple Control
**Goal:** Apply Deep Q-Learning (DQN) or Policy Gradients (REINFORCE) to solve a classic OpenAI Gym control problem (e.g., CartPole, LunarLander).
* **Focus:** Compare the performance of different reward functions and network architectures.

### 4. Zero/Few-Shot Transfer Learning with LLMs
**Goal:** Fine-tune a pre-trained large language model (e.g., a smaller open-source BERT or GPT variant) for a highly specific, low-data downstream task (e.g., legal document classification or niche domain intent detection).
* **Focus:** Evaluate performance using zero-shot, one-shot, and few-shot learning setups.

### 5. Interpreting Black-Box Models using XAI
**Goal:** Take a high-performing classification model (CNN or Transformer) and apply two different local explanation techniques (LIME and SHAP).
* **Focus:** Compare the generated explanations for consistency and robustness across multiple data points and classes.

---
