---
layout: post
title: "Are We Ready for AI to Grade Open-Ended Exams? The Collapse of an Illusion"
date: 2026-07-23
categories: RESEARCH
tags: RESEARCH
excerpt: "A deep dive into the recent findings of my graduate student's thesis, revealing why current AI models and the QWK metric fall short in grading open-ended exams."
---
<img src="/images/projects/AES-Grading.jpg" width="100%"><br>

One of the greatest excitements in the education world in recent years is the idea of artificial intelligence automatically evaluating essays and articles in open-ended exams taken by millions of students[cite: 1]. However, the results of the master's thesis successfully defended today by my graduate student Eren Demir clearly reveal that neither the world nor the Turkish National Education system is yet ready for this technological leap[cite: 1].

The problem we face when examining this issue is not merely the technological inadequacy of today's popular Large Language Models (LLMs) or BERT-based (e.g., DeBERTa) systems[cite: 1]. The actual and deeper problem is the absence in the literature of a genuinely functional evaluation metric capable of assessing a student essay holistically and semantically[cite: 1].

### The Quadratic Weighted Kappa (QWK) Illusion

Today, the success of automated scoring systems is measured by a metric called "Quadratic Weighted Kappa" (QWK)[cite: 1]. In the literature, QWK scores of 0.80 and above are considered proof that AI can grade at a "human level"[cite: 1]. Indeed, the DeBERTa-based models we developed with Eren also achieved highly successful QWK scores of 0.81-0.82 on the training data, levels that are accepted in the literature[cite: 1]. 

However, this metric cannot measure whether the model assigns a high score because it "understands" the essay or because it exploits statistical loopholes[cite: 1]. To test how "smart" our models truly are, we designed 7 different manipulation experiments on 180 essays that the models had never seen during training, and had a total of 6,870 texts rescored[cite: 1]. The results proved just how inadequate the QWK metric is as a standalone validation tool[cite: 1]:

*   **The Length Fallacy:** These supposedly successful models focus on how long the text is rather than what it actually says[cite: 1]. When filler sentences or duplicate paragraphs that contribute nothing to the content are added to the essay, the scores artificially skyrocket[cite: 1]. Conversely, when an essay is skillfully summarized while preserving its meaning, the model perceives this not as a semantic achievement but as a "mechanical truncation," and ruthlessly deducts points[cite: 1].
*   **Blindness to Logic and Organization:** The models are completely incapable of evaluating logical consistency[cite: 1]. When we inserted statements into the text where the author refutes their own argument, or when we completely reversed the paragraph order, the models failed to notice this degradation and did not deduct any points[cite: 1].
*   **Contentless LLM Traps:** "Academic-sounding empty texts," one of the greatest dangers of the generative AI era, easily deceive the models[cite: 1]. Trap texts we generated with a language model like Claude, which possess flawless surface grammar but actually mean absolutely nothing, received scores far above what they deserved (an average of +0.67 to +1.37 points) simply because of their high word counts[cite: 1].

### What Does This Mean for Educational Policies?

Eren's work has proven that an AI producing scores consistent with humans on a naturally distributed test set does not guarantee that it awards those scores for the right reasons[cite: 1]. This demonstrates that the automated scoring of open-ended exams is not just an accuracy problem, but also a massive **fairness** problem[cite: 1]. While poor writers who use simple tricks to prolong their essays are rewarded, students who write concisely and with high quality become victims of the system[cite: 1].

Deploying these systems as standalone decision-makers in high-stakes educational exams poses a significant danger[cite: 1]. The future lies not in systems where AI removes humans from the loop, but in "hybrid" scoring setups where human oversight is central, and which can generate alerts against the single-channel deviations of the model[cite: 1]. 

At least for now!
