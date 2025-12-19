---
title: "Project Task: Sectoral ReAct Agent Design"
date: 2025-1-1
categories: [NLP, Agent, AI]
tags: [react, llm, rag, agent]
description: "A task to transform a static LLM into an autonomous ReAct Agent capable of reasoning and using external tools to solve problems."
---

[cite_start]In this project, you will transform a static Language Model (LLM) that gives fixed answers into an **Autonomous Agent (ReAct Agent)** that thinks, decides, and solves problems using external resources[cite: 1018].

## 🎯 Project Goal

[cite_start]Using the provided base code skeleton, your goal is to develop a specialized AI assistant for a specific commercial field of your choice (e.g., E-Commerce, Law, Health, Logistics, etc.)[cite: 1020].
[cite_start]Your agent must answer user questions by "reasoning" using technical documents or data belonging to that sector[cite: 1021].

## 🔗 Resources

* [cite_start]**Base Code (Notebook):** <A href="https://colab.research.google.com/drive/1P_6jWDjVKEgOgPZXxUCXleyg5ERIt4Pl?usp=sharing"> Google Colab Link</a>
* **Theoretical Guide:** <A href="https://uorhan.github.io/files/Agent.pdf">*ReAct - Reasoning and Action.pdf*</a>

---

## 📝 Step-by-Step Instructions

### Step 1: Sector and Business Model Selection
Each student must choose a **different** field. [cite_start]The chosen field must have an aspect that requires "technical knowledge"[cite: 1028].
* [cite_start]*Examples:* Insurance Policy Assistant, Crypto Currency Analyst, Drug Prospectus Expert, Zoning Regulation Advisor, etc.[cite: 1030].

### Step 2: Data Collection and Knowledge Base Creation
Collect public data belonging to your chosen sector. [cite_start]You can choose one of two ways to teach this data to your model[cite: 1032]:

* [cite_start]**Path A (RAG - Recommended):** Split your data into "chunks", extract their embeddings, and save them to a Vector Database (Chroma/Pinecone, etc.)[cite: 1033].
* [cite_start]**Path B (LoRa):** Train a LoRa adapter possessing sectoral knowledge by fine-tuning a Base Model (e.g., Qwen, Llama, Mistral, etc.) with your data[cite: 1034].

### Step 3: Transition to ReAct Architecture (Most Critical Step)
[cite_start]You must perform the following integration using the provided Colab code[cite: 1036]:

1.  **Define RAG/LoRa as a "Tool":**
    * Classic RAG systems take the question and give the answer. [cite_start]In ReAct architecture, your system must be a function (Tool) that returns **raw information (context)**, not the answer[cite: 1040].
    * [cite_start]Your function must be a tool that the Agent (LLM) can call when needed (e.g., `insurance_policy_search_tool`)[cite: 1041].

2.  **System Prompt Design:**
    * Design your Agent's brain. [cite_start]Write a prompt that explains to it which tools it has and how it should think (Thought -> Action -> Observation)[cite: 1044].

### Step 4: Scenario Tests
[cite_start]Test your agent in the following two scenario types and save the logs[cite: 1046]:

* **Scenario A (One-Shot Query):** Answers to be found directly from the document.
    * [cite_start]*Ex:* "How many days is the cancellation period for X insurance?" [cite: 1047-1049].
* **Scenario B (Multi-Hop Query):** Questions that require the Agent to first pull information from the document and then make a logical inference with this information.
    * *Ex:* "Find last year's turnover from the report and convert it to TL using today's dollar exchange rate." (This requires both report reading and calculation/exchange rate knowledge) [cite_start][cite: 1050-1051].

---

## 📦 Deliverables

1.  [cite_start]**Github Repository:** [cite: 1053]
    * Working `.ipynb` (Colab) file or Python scripts.
    * `requirements.txt` used.
    * Examples from the selected dataset.
2.  [cite_start]**Project Report (PDF):** [cite: 1058]
    * Selected sector and reason.
    * Method Used (RAG or LoRa?) and architecture diagram.
    * **Trace Outputs:** Example logs showing the Agent's "Thinking" steps (Thought, Action, Observation).
    * Challenges encountered (e.g., Entering an infinite loop, hallucination, etc.) and your solutions.

---

## 💡 Tips and Warnings

* **Infinite Loop:** Sometimes if the Agent cannot find the answer, it may constantly make the same search. [cite_start]Do not forget to put a loop limit (`max_turns`) (e.g., Maximum 5 steps) [cite: 1067-1068].
* **Hallucination:** The Agent may try to invent and call a tool it does not have (e.g., `email_sender`). [cite_start]Define your tools very clearly in the System Prompt[cite: 1069].
* **Language Issue:** If your data is in English and questions are in Turkish, the Agent may get confused. [cite_start]You can solve this by giving the command "Always think and answer in Turkish" inside the Prompt [cite: 1070-1071].
