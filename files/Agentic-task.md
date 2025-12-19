---
title: "Project Task: Sectoral ReAct Agent Design"
date: 2025-1-1
description: "A task to transform a static LLM into an autonomous ReAct Agent capable of reasoning and using external tools to solve problems."
---

In this project, you will transform a static Language Model (LLM) that gives fixed answers into an **Autonomous Agent (ReAct Agent)** that thinks, decides, and solves problems using external resources.

## 🎯 Project Goal

Using the provided base code skeleton, your goal is to develop a specialized AI assistant for a specific commercial field of your choice (e.g., E-Commerce, Law, Health, Logistics, etc.).
Your agent must answer user questions by "reasoning" using technical documents or data belonging to that sector.

## 🔗 Resources

* **Base Code (Notebook):** <A href="https://colab.research.google.com/drive/1P_6jWDjVKEgOgPZXxUCXleyg5ERIt4Pl?usp=sharing"> Google Colab Link</a>
* **Theoretical Guide:** <A href="https://uorhan.github.io/files/Agent.pdf">*ReAct - Reasoning and Action.pdf*</a>

---

## 📝 Step-by-Step Instructions

### Step 1: Sector and Business Model Selection
Each student must choose a **different** field. The chosen field must have an aspect that requires "technical knowledge".
* *Examples:* Insurance Policy Assistant, Crypto Currency Analyst, Drug Prospectus Expert, Zoning Regulation Advisor, etc.

### Step 2: Data Collection and Knowledge Base Creation
Collect public data belonging to your chosen sector. You can choose one of two ways to teach this data to your model:

* **Path A (RAG - Recommended):** Split your data into "chunks", extract their embeddings, and save them to a Vector Database (Chroma/Pinecone, etc.).
* **Path B (LoRa):** Train a LoRa adapter possessing sectoral knowledge by fine-tuning a Base Model (e.g., Qwen, Llama, Mistral, etc.) with your data.

### Step 3: Transition to ReAct Architecture (Most Critical Step)
You must perform the following integration using the provided Colab code:

1.  **Define RAG/LoRa as a "Tool":**
    * Classic RAG systems take the question and give the answer. In ReAct architecture, your system must be a function (Tool) that returns **raw information (context)**, not the answer.
    * Your function must be a tool that the Agent (LLM) can call when needed (e.g., `insurance_policy_search_tool`).

2.  **System Prompt Design:**
    * Design your Agent's brain. Write a prompt that explains to it which tools it has and how it should think (Thought -> Action -> Observation).

### Step 4: Scenario Tests
Test your agent in the following two scenario types and save the logs:

* **Scenario A (One-Shot Query):** Answers to be found directly from the document.
    * *Ex:* "How many days is the cancellation period for X insurance?".
* **Scenario B (Multi-Hop Query):** Questions that require the Agent to first pull information from the document and then make a logical inference with this information.
    * *Ex:* "Find last year's turnover from the report and convert it to TL using today's dollar exchange rate." (This requires both report reading and calculation/exchange rate knowledge).

---

## 📦 Deliverables

1.  **Github Repository:**
    * Working `.ipynb` (Colab) file or Python scripts.
    * `requirements.txt` used.
    * Examples from the selected dataset.
2.  **Project Report (PDF):** 
    * Selected sector and reason.
    * Method Used (RAG or LoRa?) and architecture diagram.
    * **Trace Outputs:** Example logs showing the Agent's "Thinking" steps (Thought, Action, Observation).
    * Challenges encountered (e.g., Entering an infinite loop, hallucination, etc.) and your solutions.

---

## 💡 Tips and Warnings

* **Infinite Loop:** Sometimes if the Agent cannot find the answer, it may constantly make the same search. Do not forget to put a loop limit (`max_turns`) (e.g., Maximum 5 steps).
* **Hallucination:** The Agent may try to invent and call a tool it does not have (e.g., `email_sender`). Define your tools very clearly in the System Prompt.
* **Language Issue:** If your data is in English and questions are in Turkish, the Agent may get confused. You can solve this by giving the command "Always think and answer in Turkish" inside the Prompt.
