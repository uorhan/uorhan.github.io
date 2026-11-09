---
title: "NLP Project III: Long Document Summarization & Context Window Management"
date: 2026-9-15
---

## General Information

| Weight | Due | Defense |
|--------|-----|---------|
| 20% | Week 14 (December 20, 2026, 23:59) | Video presentation and final oral exam (see below) |

* **Tools:** The project must be implemented in Python using **local open-source LLMs via the Ollama ecosystem**. Cloud APIs (like OpenAI) are strictly forbidden.
* **Team:** The project is done individually.
* **Submission:** By **December 20, 2026, 23:59**, submit the following through the submission form (see Rules below):
  1. the YouTube link of your video,
  2. a link to your well-documented Jupyter Notebook (or Python scripts) and your brief technical report (PDF, max. 4 pages) explaining your methodology and evaluation results. Share them as a GitHub repository or a Google Drive folder with "Anyone with the link can view" access. Do not change the code or the report after the deadline.
* **Reproducibility:** State the exact model name, tag and quantization level (e.g., `llama3.1:8b-instruct-q4_K_M`), the Ollama version, and all generation parameters (temperature, seed, context length). Fix the `seed` wherever possible.

---

## Objective

To understand and overcome the hardware limitations and context window boundaries of local Large Language Models when processing large documents.

## Task Description

You are given a long document (e.g., a book chapter, a long research paper, or a financial report) that significantly exceeds the context window (token limit) of your chosen local model. You must design a pipeline to summarize the entire text without losing critical information.

## Engineering Constraints

* **Context Window:** Report the context length you used (Ollama `num_ctx`) and the token count of the full document. Note that Ollama's default context length may be much smaller than the model's maximum.
* **Chunking Strategy:** You must implement a "Map-Reduce" style algorithm. Write Python code to split the document into semantically logical chunks (e.g., by paragraphs or token limits) that fit into the context window.
* **Pipeline Execution:** Summarize each chunk individually (Map phase), and then pass the combined summaries back to the LLM to generate a final master summary (Reduce phase).
* **Evaluation:** Compare your final generated summary against a human-written reference summary using **ROUGE** metrics (ROUGE-1, ROUGE-2, and ROUGE-L). As a baseline, also report the scores of a naive approach (e.g., summarizing only the truncated beginning of the document).
* **Discussion:** Discuss the "Lost in the Middle" phenomenon and whether your chunking strategy mitigated it. Check whether key facts from the beginning, middle, and end of the document appear in the final summary.

---

## Video Presentation and Defense Questions

Like Project I, Project III is presented by video. You are required to record a **video in English** in which you explain and demonstrate your own work. Since many of you will use AI assistants while writing your code, the video is the main way for me to see that you understand your code, your design decisions and your results.

### What the Video Must Include

1. **Code walkthrough:** Explain your code step by step: how you count the tokens of the document, how you split it into chunks, how you run the Map and Reduce phases through Ollama, how you build the baseline, and how you compute ROUGE.
2. **Live tests:** Run your code on screen and show at least the following:
   * The token count of the full document and the `num_ctx` value you used.
   * Your pipeline running on a part of the document (at least 3 chunks), with the Map outputs and the final summary.
   * The same part with a different chunk size, with ROUGE computed for both runs. Comment on the difference.
3. **Answers to the defense questions:** Answer all 4 questions in Section A and one question of your choice from each of Sections B–G (10 questions in total) in your own words, based on your own code and results. Answer at least one of your chosen questions with an experiment and show the result in the video.

### Rules

* Length: at most **30 minutes**. Add timestamps for the three parts to the YouTube video description (e.g., "00:00 Code walkthrough", "09:30 Live tests", "16:45 Defense questions"), so that they appear as chapters in the video. In the submission form, give the start times of the live tests and the defense questions; the code walkthrough always starts at 00:00.
* YouTube allows videos longer than 15 minutes only from verified accounts. Verify your account by phone in advance at youtube.com/verify.
* You may record the video in several parts and join them, but the live tests must be shown without cuts, from running the code to the output.
* Your **screen and voice** must be recorded throughout, and your **face must be visible** at least at the beginning of the video.
* Use the exact model, quantization level and parameters stated in your report.
* Upload your video to **YouTube as "Unlisted"**. If you choose "Private", I cannot watch it; do not choose "Public" either. Do not send the link by e-mail; submit it through this form by **December 20, 2026, 23:59**: <!-- TODO: form link -->. Only one submission per student is accepted. Your video must remain Unlisted and available until final grades are announced.
* Reading prepared answers from a script is not acceptable. Speak naturally; short pauses and mistakes are fine.
* **Final oral exam (Week 15):** Every student has an in-person oral exam in Week 15. In this exam, you are responsible for **all** defense questions of Projects I, II and III, not only the ones you answered in your videos. Your answers are taken into account in your project grades.

### Defense Questions

*Answer all questions in Section A and one question from each of Sections B–G in your video. In the final oral exam, you are responsible for all questions.*

#### A. Your Code and Results (all required)
1. Choose one line from your chunking code or your Reduce code (not an import, print or comment line). Explain what it does and show what happens when it is removed.
2. Did your AI assistant suggest anything that you decided not to use? Why not?
3. Which of your results surprised you? How do you explain it?
4. Compare the ROUGE scores of your pipeline with those of the truncated baseline. Is the difference as large as you expected? Why?

#### B. Context Window and Attention
5. What `num_ctx` value did you use, and what is the model's maximum context length? What happens in Ollama if the input is longer than `num_ctx`?
6. Why does processing time grow as the chunk size increases? Explain using attention.
7. What is the KV cache? How does it affect memory use when you increase `num_ctx`?
8. Did you observe the "Lost in the Middle" effect? How did you test it?

#### C. Chunking Strategies
9. What happens if you split the document by a fixed number of tokens instead of by paragraphs and sentences are cut in the middle?
10. What would you gain and lose by adding a 10–20% overlap between chunks?
11. How would very small or very large chunks affect ROUGE and running time?
12. How would ROUGE and running time change if you used the "refine" method (updating the previous summary with each new chunk) instead of Map-Reduce?

#### D. Evaluation
13. What is the difference between ROUGE-1, ROUGE-2 and ROUGE-L? Which one best reflects the quality of your summaries?
14. Can a summary with a high ROUGE score still be a bad summary? Give an example.
15. Why is ROUGE especially problematic for abstractive summaries in Turkish?

#### E. Hallucination and Faithfulness
16. Did your final summary contain information that is not in the document? Show an example. Did it appear in the Map phase or in the Reduce phase?
17. How would you automatically check each sentence of the final summary against the source document?

#### F. Pipeline Variations: "What if we had tried…?"
18. If you shuffled the order of the chunk summaries in the Reduce phase, would the final summary change?
19. If you gave the whole document at once to a model with a long enough context window, would it beat your Map-Reduce pipeline? What could be lost?
20. What would happen if you first selected the most important sentences with TF-IDF (extractive summarization) and then gave them to the LLM?
21. What would you do if the combined chunk summaries themselves did not fit into the context window?

#### G. Model and Prompt Choices
22. How would your results and running time change if you used a smaller (1B) or a larger (8B) model?
23. Did you use the same prompt for the Map and Reduce phases? Why or why not? How would you optimize these prompts, and on which data would you test them?
24. How did you choose your `num_ctx` value with respect to your GPU memory? What happens if it does not fit?
