---
title: "NLP Project Task: LoRA"
date: 2025-1-1
categories: [NLP, Project, LoRA, AI]
tags: [LoRA, llm, fine-tuning]
description: ""
---

# 🚀 Competitive Code Reasoning with LoRa Fine-Tuning

In this project, you will fine-tune a base model using **LoRa (Low-Rank Adaptation)** to improve its code reasoning capabilities. You will train two separate models using two different datasets and compare their performance.

## 🎯 Project Goal
To fine-tune a pre-trained "Instruct" model on two different datasets (DEEP and DIVERSE) to specialize it in code generation and reasoning, and then to evaluate the best performing checkpoint.

---

## 🛠️ Preparation & Requirements

### 1. Base Model (Mandatory)
You must use the following model for all experiments:
* **Model:** `Qwen/Qwen2.5-Coder-1.5B-Instruct`
* **Note:** This model will serve as your starting point.

### 2. Datasets
You are required to use these two datasets:
* **DEEP Dataset:** [CodeGen-Deep-5K](https://huggingface.co/datasets/Naholav/CodeGen-Deep-5K) (Contains deeper reasoning traces)
* **DIVERSE Dataset:** [CodeGen-Diverse-5K](https://huggingface.co/datasets/Naholav/CodeGen-Diverse-5K) (Contains varied problem types)

**Data Structure:**
* `input`: Problem description
* `solution`: Clean code only (No reasoning)
* `output`: Reasoning traces + code (Thinking process inside `<think>` tags)

---

## 📝 Tasks

### Task 1: Model Setup & Initial Review
1. Download and set up the base model (`Qwen2.5-Coder-1.5B-Instruct`).
2. Run inference with a few test questions.
3. Document the model's initial (baseline) capabilities.

### Task 2: Dataset Analysis
1. Download both datasets (DEEP and DIVERSE).
2. Examine the data structure locally.
3. **Crucial:** Understand the difference between the fields:
    * `solution`: Contains code only.
    * `output`: Contains reasoning (`<think>` tags) + code.
4. **Instruction:** For this project, you will primarily train using the **`solution` field** (code-only).

### Task 3: Training (Fine-Tuning)
You will perform 2 separate training sessions starting from the same base model:

**Training A: DEEP Dataset**
* Base: `Qwen2.5-Coder-1.5B-Instruct`
* Data: DEEP Dataset
* Field: Use the `solution` field.

**Training B: DIVERSE Dataset**
* Base: `Qwen2.5-Coder-1.5B-Instruct`
* Data: DIVERSE Dataset
* Field: Use the `solution` field.

> **Warning:** Both trainings must start from the base model. Do not continue training from one to the other.

### Task 4: Checkpoint Selection
1. You will obtain multiple checkpoints during training (e.g., `checkpoint-step-400`, `checkpoint-step-500`).
2. Evaluate each checkpoint using the test split of your dataset.
3. Select the best-performing checkpoint for each training session.

### Task 5: Final Evaluation & Submission
You will evaluate your models on a benchmark dataset (to be released later) and prepare a presentation.

---

## ⚙️ Recommended Technical Configuration

These values are recommendations; you may adjust them based on your experiments:

* **LoRa Rank (r):** 16, 32, or 64
* **Alpha:** 2x Rank (e.g., if r=16, alpha=32)
* **Target Modules:** Apply LoRa to both Attention and MLP layers.
* **Dropout:** Enable LoRa dropout.
* **Epochs:** ~3 epochs
* **Context Length:** 1024 tokens (for solution-only training)
* **Optimizer:** AdamW (fused=True) with Cosine Decay scheduler.
* **Effective Batch Size:** 16 (Use gradient accumulation if needed).

**System Prompt (Mandatory):**
> "You are an expert Python programmer. Please read the problem carefully before writing any Python code."

---

## ⚠️ Troubleshooting (OOM - Out of Memory)
If you encounter CUDA Out of Memory errors, try these steps in order:
1. Enable **Flash Attention 2**.
2. Enable **Gradient Checkpointing**.
3. Reduce **Context Length** (Minimum 800 tokens).
4. (Last Resort) Use **8-bit quantization** (`adamw_8bit`).

---

## 📦 Deliverables (Checklist)

Before submitting, ensure you have the following:

* [ ] **Two Trained Models:** (DEEP and DIVERSE versions)
* [ ] **GitHub Repository:**
    * Training scripts
    * Evaluation scripts
    * Training logs (Train loss every 20-40 steps, Validation loss every 100-120 steps)
* [ ] **HuggingFace Model Cards:** For both models.
* [ ] **Report/Presentation:** 1-2 pages summarizing hyperparameters and results.
