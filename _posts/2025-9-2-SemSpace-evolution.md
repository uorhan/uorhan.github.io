---
layout: post
title: "🧭 SemSpace: The Birth of a Universe of Meaning"
subtitle: "Evolution of Semspace algorithm"
date: 2025-9-2
categories: PROJECT
excerpt: "From a simple graph-based experiment to a universe of meaning — this is the eight-year journey of SemSpace, a model that redefined how machines understand language."
---
<img src="/images/projects/SemSpace-evolution.jpg" witdth="100%"><br>
This article tells the short history of a long journey—from graphs to vector spaces.  
Let’s examine, step by step, how we evolved from our earliest graph-based experiments in NLP to increasingly complex semantic-space algorithms.

---

## 1. The First Sparks: 2016  

Everything began in 2016 with the acceptance of our nationally funded project, *“Designing a Dynamic Turkish Dictionary Network Using Weighted Graphs.”*  
I prepared the proposal together with my linguist colleague **Dr. Tahir Tahiroğlu** and my PhD students **Erhan Turan** and **Enis Arslan**. Yet another doctoral student, **Çağatay Neftali Tulu**, would later transcend the limits of this graphical infrastructure and create an entirely new paradigm.  

Our goal was to represent morphological and semantic relations between Turkish words as a network—essentially, to build a “living dictionary web” connecting affixes and meaning layers dynamically.  
I still remember the excitement we felt when the approval letter arrived. From that moment, the real journey began.

---

## 2. Language on Graphs (2016–2017)  

The early years were filled with brilliant ideas—but implementation revealed fundamental NLP challenges.  
During this period, **Enis Arslan** modeled Turkish root-affix relations in graph form:  
- *Graph-based Lemmatization of Turkish Words by Using Morphological Similarity* (INISTA 2016)  
- *Using Graphs in Construction of a Lemmatization Model for Turkish* (IMSEC 2017)  

Meanwhile, **Çağatay Tulu** quantified semantic proximity between words by applying the PageRank algorithm to measure inter-node distances:  
- *PageRank-Based Semantic Similarity Measure on a Graph-Based Turkish WordNet* (UBMK 2017)  

At this stage, we proved to ourselves that semantic relations among Turkish words could be measured mathematically—an insight that led us toward even bigger questions.

---

## 3. Deepening the Semantic Network (2018)  

The year 2018 marked the maturation of our “semantic network.”  
Together with **Erhan Turan**, **Çağatay Tulu**, **Enis Arslan**, and **Tahir Tahiroğlu**, we published numerous symposium papers:  
- *Building a Turkish Semantic Network and Connecting Synonym Senses Bidirectionally* (INISTA 2018)  
- *Using Graph Connectivity Measures for Distance in Semantic Networks* (Computational Math. & Eng. Sciences 2018)  
- *Determination of Semantic Relations Weight’s on WordNet* (2018)  
- *Morphological Disambiguation of Turkish with Free-Order Co-Occurrence Statistics* (Arslan, Orhan, Tahiroğlu 2018)  
- *Semantic Relation’s Weight Determination on a Graph-Based WordNet* (Tulu, Orhan, Turan 2018)  

These studies strengthened our vision of merging morphological analysis and semantic similarity within a single mathematical framework. Words were no longer just *connected*—they became quantifiable semantic entities.

---

## 4. A Turning Point Shaped by Doctoral Theses (2019–2020)  

At this stage, my students’ doctoral dissertations—especially Çağatay’s—laid the foundation for SemSpace.  

**Çağatay Neftali Tulu** (PhD, June 2019)  
*“A Semantic Vector Space Model Using Euclidean Distance Based Relatedness”*  
— the first step from the graph structure of English WordNet into geometric space, where meaning could now be expressed as a distance function.  
While converting categorical semantic relations into numerical weights, a dual-optimization algorithm I developed in Matlab yielded impressive results. We later adapted this algorithm to Enis’s morphological-disambiguation studies.  

**Enis Arslan** (PhD, January 2020)  
*“Learning Word-Vector Quantization: A Study in Morphological Disambiguation of Turkish”*  
— solved the root-affix separation problem through vector quantization, reinforcing the core learning mechanism of SemSpace.  

Meanwhile, **Erhan Turan** took an entirely different perspective by focusing on dictionary definitions:  

**Erhan Turan** (PhD, April 2020)  
*“Automatic Synset Detection from Turkish Dictionary Using Confidence Indexing”*  
— he identified the lack of standardization in Turkish dictionary definitions and quantified it with a measure we called the *Confidence Index*, paving the way for machine-readable dictionaries across languages.  

Complementary papers reinforced this trajectory:  
- *Identification of OOV Words in Turkish Texts* (Arslan & Orhan 2019)  
- *Learning Word-Vector Quantization* (Orhan & Arslan, TALLIP 2020)  
- *A Comparison of Graph Centrality Algorithms for Semantic Distance* (Turan, Arslan, Tulu, Orhan 2020)

---

## 5. The Official Birth of SemSpace (2021)  

After years of research, 2021 brought the true milestone.  
With our paper in *Expert Systems with Applications*, SemSpace was formally introduced to the scientific world:  
> *“A Novel Embedding Approach to Learn Word Vectors by Weighting Semantic Relations: SemSpace.”*  

This method derived meaning not from mere statistical co-occurrence but from the weighted structure of semantic relations themselves.  
It was a major achievement—yet I still felt something missing. I wanted to show how SemSpace could engage with real-world problems.  

I remembered the fill-in-the-blank exam questions I used in class. That memory sparked a new goal: **automatic short-answer grading.**  
In our *IEEE Access (2021)* paper with **Özge Özkaya** and **Çağatay**, we demonstrated how SemSpace vectors could be used for short-answer assessment.  
Now the model was not only analyzing language but also performing effective evaluation.

---

## 6. Context, Meaning, and Intent Detection (2022–2023)  

During exam assessments, I noticed something: even though tests measured knowledge, students struggled with interpretive questions. That led me to a deeper question—*what does it mean to understand?*  

Understanding was the key; an AI that failed to understand could never respond appropriately. The problem was vast, so we focused on a subset: **intent detection** in natural language.  
This time, PhD student **Elif Gülfidan Tosun Dayıoğlu** took the stage. Her dissertation carried SemSpace into contextual territory:  

**Elif Gülfidan Tosun Dayıoğlu** (PhD, September 2023)  
*“Contextualized Intent Detection Using Generalized SemSpace and BLSTM”*  

Together with the paper published in *Arabian Journal for Science and Engineering (2023)*, this study launched the **Deep SemSpace era**. SemSpace could now comprehend not only words but also **intent** and **context**.

---

## 7. Today and Beyond  

Over eight years, SemSpace evolved from a simple graph project into a **universe of meaning**. Each thesis and paper added a new layer to this universe.  
Today, SemSpace stands not only as a model for Turkish semantic analysis but as part of a broader scientific legacy questioning the **measurability of meaning**.  

And the story is still being written.  
Although we have paused briefly amid the rise of large language models, the SemSpace journey is far from over—  
perhaps very soon, we’ll return to the stage with a **new LLM-enhanced SemSpace**.
