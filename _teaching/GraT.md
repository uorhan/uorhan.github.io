---
title: Graph Theory
collection: teaching
type: "PhD Course"
permalink: /teaching/GraT
venue: "CuCEng"
date: 2025-1-1
---

## Course Description
This course is designed for PhD students to explore the mathematical foundations of graph theory, analyze complex networks, and transition into modern graph representation learning (GNNs). The course follows a **seminar-based format**. Students are expected to read the assigned seminal paper or book chapter before class and participate in critical discussions.

Instead of traditional written exams, evaluation is based on weekly paper critiques and a hands-on term project that solves a research problem using graph-based methods.

## Recommended Textbooks
1.  **Reinhard Diestel**, *Graph Theory* (5th Edition).
2.  **M.E.J. Newman**, *Networks: An Introduction*.
3.  **William L. Hamilton**, *Graph Representation Learning*.

---

## Assessment and Evaluation
| Component | Weight | Description |
| :--- | :--- | :--- |
| **Weekly Paper Critique** | 40% | Critical reading and active discussion during seminars. |
| **Final Project** | 60% | Implementation code, final report, and presentation. |

---

### Weekly Schedule and Reading List

The curriculum is divided into three modules: **Classical Theory**, **Network Science**, and **Deep Learning on Graphs**.

| Week | Topic | Primary Reading (Paper/Chapter) |
| :--- | :--- | :--- |
| **1** | **Foundations & Matching** <br> (Connectivity, Paths, Hall's Condition) | **Book Chapter:** Diestel, R. *Graph Theory*, Chapters 1 & 2. |
| **2** | **Extremal Graph Theory** <br> (Turán Graphs & Ramsey Theory basics) | **Paper:** Bollobás, B. (1978). *Extremal Graph Theory*. (Focus on Turán's Theorem). |
| **3** | **Spectral Graph Theory** <br> (The Laplacian & Eigenvalues) | **Paper:** Spielman, D. A. (2007). *Spectral Graph Theory and its Applications*. (FOCS Tutorial). |
| **4** | **Random Graphs** <br> (The Erdős–Rényi Model) | **Classic:** Erdős, P., & Rényi, A. (1959). *On Random Graphs I*. Publicationes Mathematicae. |
| **5** | **Small-World Networks** <br> (Clustering Coefficients & Path Lengths) | **Classic:** Watts, D. J., & Strogatz, S. H. (1998). *Collective dynamics of 'small-world' networks*. Nature. |
| **6** | **Scale-Free Networks** <br> (Power Laws & Preferential Attachment) | **Classic:** Barabási, A. L., & Albert, R. (1999). *Emergence of scaling in random networks*. Science. |
| **7** | **Community Detection** <br> (Modularity Optimization) | **Paper:** Newman, M. E., & Girvan, M. (2004). *Finding and evaluating community structure in networks*. Physical Review E. |
| **8** | **Midterm Week / Proposal Defense** | *Presentation of Term Project Proposals and Literature Review.* |
| **9** | **Network Motifs** <br> (Building Blocks of Complex Networks) | **Paper:** Milo, R. et al. (2002). *Network motifs: simple building blocks of complex networks*. Science. |
| **10** | **Node Embeddings** <br> (Shallow Encoders: DeepWalk/Node2Vec) | **Paper:** Grover, A., & Leskovec, J. (2016). *node2vec: Scalable feature learning for networks*. KDD. |
| **11** | **Graph Convolutional Networks** <br> (GCNs & Spectral Filtering) | **Paper:** Kipf, T. N., & Welling, M. (2017). *Semi-Supervised Classification with Graph Convolutional Networks*. ICLR. |
| **12** | **Inductive Representation Learning** <br> (GraphSAGE & Attention Mechanisms) | **Paper:** Veličković, P. et al. (2018). *Graph Attention Networks (GAT)*. ICLR. |
| **13** | **Generative Graph Models** <br> (GraphRNN or VAEs for Graphs) | **Paper:** You, J. et al. (2018). *GraphRNN: Generating Realistic Graphs with Deep Auto-regressive Models*. ICML. |
| **14** | **Final Project Presentations** | *Demo and technical report presentation.* |

---

## Sample Project Topics

Students can select one (or propose another) topic, implement a solution, and write a conference-style paper (4-6 pages).

### 1. Link Prediction in Citation Networks
**Goal:** Predict missing citations in the Cora or CiteSeer dataset.
* **Methodology:** Compare heuristic methods (Adamic-Adar, Jaccard) against embedding-based methods (Node2Vec) and GNNs (VGAE).

### 2. Misinformation Spread Analysis (Social Network Analysis)
**Goal:** Model the diffusion of "fake news" using Twitter (X) or Reddit data.
* **Methodology:** Identify "Super-spreaders" using Centrality measures (Betweenness, Eigenvector) and simulate cascade dynamics.

### 3. Functional Module Detection in PPI Networks
**Goal:** Analyze Protein-Protein Interaction networks to find biologically relevant clusters.
* **Methodology:** Implement Spectral Clustering and optimize Modularity to detect communities; validate against Gene Ontology terms.

### 4. Robustness of Power Grids or Transport Networks
**Goal:** Simulate attacks on a critical infrastructure network.
* **Methodology:** Remove nodes based on degree vs. random removal to test network resilience (Giant Component size) and propose defense strategies.

### 5. Recommender System with Bipartite Graphs
**Goal:** Build a movie or product recommender using the MovieLens dataset.
* **Methodology:** Model User-Item interactions as a bipartite graph and utilize GraphSAGE or LightGCN for link prediction.

### 6. Combinatorial Optimization with GNNs
**Goal:** Solve NP-Hard problems (e.g., Traveling Salesman Problem or Maximum Cut) using deep learning.
* **Methodology:** Train a Pointer Network or GNN to approximate the solution and compare run-time/accuracy against classical heuristics.

---

