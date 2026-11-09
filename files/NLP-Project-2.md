---
title: "NLP Project II: Translation, Paraphrasing, and Metric Evaluation"
date: 2026-11-9
---

## General Information

| Weight | Due | Defense |
|--------|-----|---------|
| 20% | Week 12 (December 6, 2026, 23:59) | Video presentation and final oral exam (see below) |

* **Tools:** The project must be implemented in Python using **local open-source LLMs via the Ollama ecosystem**. Cloud APIs (like OpenAI) are strictly forbidden.
* **Team:** The project is done individually.
* **Submission:** By **December 6, 2026, 23:59**, submit the following through the submission form (see Rules below):
  1. the YouTube link of your video,
  2. a link to your well-documented Jupyter Notebook (or Python scripts) and your brief technical report (PDF, max. 4 pages) explaining your methodology and evaluation results. Share them as a GitHub repository or a Google Drive folder with "Anyone with the link can view" access. Do not change the code or the report after the deadline.
* **Reproducibility:** State the exact model name, tag and quantization level (e.g., `llama3.1:8b-instruct-q4_K_M`), the Ollama version, and all generation parameters (temperature, seed, context length). Fix the `seed` wherever possible.

---

## Objective

To analyze the generative capabilities of LLMs in translation and style transfer, and to scientifically evaluate their output quality using standard NLP metrics rather than subjective human evaluation.

## Task Description

Select a dataset containing source texts and their reference translations (or paraphrased versions). Instruct the local LLM to translate the text or rewrite it in a different tone (e.g., from informal to academic). Use at least 100 source–reference pairs for evaluation.

## Engineering Constraints

* **Metric Calculation:** You must computationally evaluate the LLM's outputs against the ground-truth reference texts using **BLEU**, **METEOR**, and **chrF** (e.g., with `sacrebleu`, NLTK, or Hugging Face `evaluate`). Report corpus-level scores and state which library and settings you used (for `sacrebleu`, include the signature). Adding **BERTScore** as a semantic metric is optional but encouraged.
* **Turkish Data:** If your target language is Turkish, discuss how the language's agglutinative morphology affects word-level metrics (BLEU, METEOR) compared with character-level chrF.
* **Hyperparameter Analysis:** Run the same task using at least three different `temperature` values (e.g., 0.1, 0.7, 1.2), keeping all other parameters fixed.
* **Deliverable:** Plot a graph showing how changing the temperature affects each metric and write a brief analysis discussing the trade-off between determinism and creativity. Include at least 5 examples where the metrics disagree with your own judgment of quality.

---

## Video Presentation and Defense Questions

Like Project I, Project II is presented by video. You are required to record a **video in English** in which you explain and demonstrate your own work. Since many of you will use AI assistants while writing your code, the video is the main way for me to see that you understand your code, your design decisions and your results.

### What the Video Must Include

1. **Code walkthrough:** Explain your code step by step: how you load the data, how you build the prompt, how you call the model through Ollama, how you compute BLEU, METEOR and chrF, and how you produce the temperature graph.
2. **Live tests:** Run your code on screen and show at least the following:
   * The same 5 sentences translated (or paraphrased) at two different temperature values, with the metrics computed live.
   * One example from your data where the metrics disagree with your own judgment. Explain why.
   * At least 3 new sentences that are not in your dataset, including one that you expect the model to get wrong (e.g., an idiom or a technical term). Comment on the outputs.
3. **Answers to the defense questions:** Answer all 4 questions in Section A and one question of your choice from each of Sections B–G (10 questions in total) in your own words, based on your own code and results. Answer at least one of your chosen questions with an experiment and show the result in the video.

### Rules

* Length: at most **30 minutes**. Add timestamps for the three parts to the YouTube video description (e.g., "00:00 Code walkthrough", "09:30 Live tests", "16:45 Defense questions"), so that they appear as chapters in the video. In the submission form, give the start times of the live tests and the defense questions; the code walkthrough always starts at 00:00.
* YouTube allows videos longer than 15 minutes only from verified accounts. Verify your account by phone in advance at youtube.com/verify.
<!-- TODO: video editing rule — same option as Project I -->
* Your **screen and voice** must be recorded throughout, and your **face must be visible** at least at the beginning of the video.
* Use the exact model, quantization level and parameters stated in your report.
* Upload your video to **YouTube as "Unlisted"**. If you choose "Private", I cannot watch it; do not choose "Public" either. Do not send the link by e-mail; submit it through this form by **December 6, 2026, 23:59**: <!-- TODO: form link -->. Only one submission per student is accepted. Your video must remain Unlisted and available until final grades are announced.
* Reading prepared answers from a script is not acceptable. Speak naturally; short pauses and mistakes are fine.
* **Final oral exam (Week 15):** Every student has an in-person oral exam in Week 15. In this exam, you are responsible for **all** defense questions of Projects I, II and III, not only the ones you answered in your videos. Your answers are taken into account in your project grades.

### Defense Questions

*Answer all questions in Section A and one question from each of Sections B–G in your video. In the final oral exam, you are responsible for all questions.*

#### A. Your Code and Results (all required)
1. Choose one line from your prompt-building code or your metric code (not an import, print or comment line). Explain what it does and show what happens when it is removed.
2. Did your AI assistant suggest anything that you decided not to use? Why not?
3. Which of your results surprised you? How do you explain it?
4. Show one example where BLEU and chrF disagree. Why do they disagree?

#### B. Evaluation Metrics
5. Why can a correct Turkish translation get a low BLEU score when its suffixes differ from the reference? Show an example from your data.
6. What is the difference between corpus-level and sentence-level BLEU? Which one did you report, and why?
7. If you used a translation by another translator as the reference, how much would your scores change? What does this tell you about the metric?
8. How would BLEU change if you had more than one reference translation per sentence?
9. Why can BERTScore give a high score to a translation that BLEU scores low? Is a high BERTScore always a good sign?

#### C. Generation Parameters
10. How did your metrics change across the three temperature values? Explain the trade-off between determinism and creativity using your graph.
11. At a high temperature, does the same sentence get the same translation twice? How did you take this into account in your measurements?
12. Would you choose the same temperature for paraphrasing (style transfer) as for translation? Why?

#### D. Hallucination and Groundedness
13. Did you see a translation that adds information or leaves out part of the source? Show an example. Which metric catches it, and which does not?
14. How would you automatically detect that a translation leaves out part of the source sentence?
15. If you gave the model a glossary of terms, would term errors decrease? How would you measure this?

#### E. Tokenization and Context
16. Why does a Turkish sentence contain more tokens than its English translation? How does this affect the speed of your pipeline?
17. If you translated several sentences together instead of one at a time, how would BLEU and speed change? What could go wrong when you match outputs to references?

#### F. Prompt Strategies: "What if we had tried…?"
18. If you added 3 example translations to the prompt (few-shot), would BLEU increase? Would this mean a better translation, or only a style closer to the references?
19. What would happen if you translated first into English and then into the target language (pivot translation)?
20. For paraphrasing, if you asked the model to "rewrite with as few words as possible" instead of "keep the same meaning", how would METEOR change?
21. How would you optimize your system prompt? On which data would you run your trials, and why should you not run them on the test data?

#### G. Model Choices
22. How would your metrics and speed change if you used a smaller (1B) or a larger (8B) model?
23. Would a more aggressive quantization (e.g., 4-bit instead of 8-bit) affect translation quality? How would you measure it?
24. Would a model trained mostly on English data translate into Turkish worse than into English? How would you test this?
