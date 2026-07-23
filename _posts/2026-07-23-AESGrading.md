---
layout: post
title: "Are We Ready for AI to Grade Open-Ended Exams? The Collapse of an Illusion"
date: 2026-07-23
categories: RESEARCH
tags: RESEARCH
excerpt: "A deep dive into the recent findings of my graduate student's thesis, revealing why current AI models and the QWK metric fall short in grading open-ended exams."
---
<img src="/images/projects/AES-Grading.jpg" width="100%"><br>

One of the greatest excitements in the education world in recent years is the idea of artificial intelligence automatically evaluating essays and articles in open-ended exams taken by millions of students. However, the results of the master's thesis successfully defended today by my graduate student Eren Demir clearly reveal that neither the world nor the Turkish National Education system is yet ready for this technological leap.

The problem we face when examining this issue is not merely the technological inadequacy of today's popular Large Language Models (LLMs) or BERT-based (e.g., DeBERTa) systems. The actual and deeper problem is the absence in the literature of a genuinely functional evaluation metric capable of assessing a student essay holistically and semantically.

### The Quadratic Weighted Kappa (QWK) Illusion

Today, the success of automated scoring systems is measured by a metric called "Quadratic Weighted Kappa" (QWK). In the literature, QWK scores of 0.80 and above are considered proof that AI can grade at a "human level". Indeed, the DeBERTa-based models we developed with Eren also achieved highly successful QWK scores of 0.81-0.82 on the training data, levels that are accepted in the literature. 

However, this metric cannot measure whether the model assigns a high score because it "understands" the essay or because it exploits statistical loopholes. To test how "smart" our models truly are, we designed 7 different manipulation experiments on 180 essays that the models had never seen during training, and had a total of 6,870 texts rescored. The results proved just how inadequate the QWK metric is as a standalone validation tool:

*   **The Length Fallacy:** These supposedly successful models focus on how long the text is rather than what it actually says. When filler sentences or duplicate paragraphs that contribute nothing to the content are added to the essay, the scores artificially skyrocket. Conversely, when an essay is skillfully summarized while preserving its meaning, the model perceives this not as a semantic achievement but as a "mechanical truncation," and ruthlessly deducts points.
*   **Blindness to Logic and Organization:** The models are completely incapable of evaluating logical consistency. When we inserted statements into the text where the author refutes their own argument, or when we completely reversed the paragraph order, the models failed to notice this degradation and did not deduct any points.
*   **Contentless LLM Traps:** "Academic-sounding empty texts," one of the greatest dangers of the generative AI era, easily deceive the models. Trap texts we generated with a language model like Claude, which possess flawless surface grammar but actually mean absolutely nothing, received scores far above what they deserved (an average of +0.67 to +1.37 points) simply because of their high word counts.

### What Does This Mean for Educational Policies?

Eren's work has proven that an AI producing scores consistent with humans on a naturally distributed test set does not guarantee that it awards those scores for the right reasons. This demonstrates that the automated scoring of open-ended exams is not just an accuracy problem, but also a massive **fairness** problem. While poor writers who use simple tricks to prolong their essays are rewarded, students who write concisely and with high quality become victims of the system.

Deploying these systems as standalone decision-makers in high-stakes educational exams poses a significant danger. The future lies not in systems where AI removes humans from the loop, but in "hybrid" scoring setups where human oversight is central, and which can generate alerts against the single-channel deviations of the model. 

At least for now!
