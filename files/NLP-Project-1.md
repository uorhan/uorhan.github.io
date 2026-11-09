---
title: "NLP Project I: Structured Text Classification & Information Extraction"
date: 2026-11-09
---

## General Information

| Weight | Due | Defense |
|--------|-----|---------|
| 20% | Week 10 (November 22, 2026, 23:59) | Video presentation and final oral exam (see below) |

* **Tools:** The project must be implemented in Python using **local open-source LLMs via the Ollama ecosystem**. Cloud APIs (like OpenAI) are strictly forbidden.
* **Team:** The project is done individually.
* **Submission:** By **November 22, 2026, 23:59**, submit the following through the submission form (see Rules below):
  1. the YouTube link of your video,
  2. a link to your well-documented Jupyter Notebook (or Python scripts) and your brief technical report (PDF, max. 4 pages) explaining your methodology and evaluation results. Share them as a GitHub repository or a Google Drive folder with "Anyone with the link can view" access. Do not change the code or the report after the deadline.
* **Reproducibility:** State the exact model name, tag and quantization level (e.g., `llama3.1:8b-instruct-q4_K_M`), the Ollama version, and all generation parameters (temperature, seed, context length). Fix the `seed` wherever possible.

---

## Objective

To move beyond conversational "black-box" LLM usage by forcing the model to generate strictly structured data that can be programmatically parsed and integrated into software systems.

## Task Description

You will use a local LLM to classify texts and extract specific entities from an unstructured dataset (e.g., IMDB reviews, Turkish news articles, or medical epikrisis reports).

* **Gold labels for entities:** Entity extraction F1 requires gold entity labels. Many datasets (e.g., IMDB) have only class labels. In that case, you must manually annotate the entities in your evaluation samples and describe your annotation rules in the report.
* **Matching entities in Turkish:** State your matching rule (exact or partial match) in the report. If you lowercase before matching, note that Python's `str.lower()` is not correct for Turkish: `'İSTANBUL'.lower()` gives `'i̇stanbul'` (with a combining dot) and `'IŞIK'.lower()` gives `'işik'`. Replace `İ` with `i` and `I` with `ı` before calling `lower()`.

## Engineering Constraints

* **No Free-Text Allowed:** The model's output must be strictly in a valid JSON format (e.g., `{"category": "sports", "sentiment_score": 0.8, "entities": ["person A", "location B"]}`).
* **Two Experimental Settings:** Run the same task in two settings and compare them:
  1. **Prompt-only:** JSON format is requested only through the prompt. The Ollama `format` parameter must **not** be used.
  2. **Schema-constrained:** The Ollama `format` parameter is used with a JSON schema.
* **Exception Handling:** In the prompt-only setting, LLMs often break formatting (e.g., adding markdown blocks like ` ```json ` or conversational text like "Here is your JSON..."). You must write Python code to clean the output, parse the JSON, and include `try-except` blocks to handle parsing failures gracefully.
* **Evaluation:** Across at least 100 samples, report for both settings:
  * Raw JSON parsing success rate: `json.loads` applied directly to the raw model output, **before** any cleaning,
  * JSON parsing success rate **after** your cleaning code,
  * Schema validity rate (all required fields present with correct types),
  * Task accuracy (classification accuracy / F1 and entity extraction F1 against gold labels).
* **Discussion:** Does schema-constrained decoding change task accuracy, not just format validity? Explain why or why not.

---

## Video Presentation and Defense Questions

Since the originally planned date for the first presentations had to be postponed for reasons beyond our control, I have made a new plan. To avoid further delays in the course schedule, Project I will be presented by video. You are required to record a **video in English** in which you explain and demonstrate your own work. Since many of you will use AI assistants while writing your code, the video is the main way for me to see that you understand your code, your design decisions and your results.

### What the Video Must Include

1. **Code walkthrough:** Explain your code step by step: how you load the data, how you build the prompt, how you call the model through Ollama, how you clean and parse the JSON output, and how you compute the evaluation metrics.
2. **Live tests:** Run your code on screen and show at least the following:
   * The same samples in both settings: prompt-only and with the `format` parameter.
   * The same samples with at least two different temperature values (e.g., 0 and 1.0).
   * At least 5 new samples that are not in your dataset, including one that you expect the model to get wrong. Comment on the outputs.
3. **Answers to the defense questions:** Answer all 4 questions in Section A and one question of your choice from each of Sections B–G (10 questions in total) in your own words, based on your own code and results. Answer at least one of your chosen questions with an experiment and show the result in the video.

### Rules

* Length: at most **30 minutes**. Add timestamps for the three parts to the YouTube video description (e.g., "00:00 Code walkthrough", "09:30 Live tests", "16:45 Defense questions"), so that they appear as chapters in the video. In the submission form, give the start times of the live tests and the defense questions; the code walkthrough always starts at 00:00.
* YouTube allows videos longer than 15 minutes only from verified accounts. Verify your account by phone in advance at youtube.com/verify.
* You may record the video in several parts and join them, but the live tests must be shown without cuts, from running the code to the output.
* Your **screen and voice** must be recorded throughout, and your **face must be visible** at least at the beginning of the video.
* Use the exact model, quantization level and parameters stated in your report.
* Upload your video to **YouTube as "Unlisted"**. If you choose "Private", I cannot watch it; do not choose "Public" either. Do not send the link by e-mail; submit it through this form by **November 22, 2026, 23:59**:  [Upload Form](https://forms.gle/sdhhRnpkZBVQ8Dnc8). Only one submission per student is accepted. Your video must remain Unlisted and available until final grades are announced.
* Reading prepared answers from a script is not acceptable. Speak naturally; short pauses and mistakes are fine.
* **Final oral exam (Week 15):** Every student has an in-person oral exam in Week 15. In this exam, you are responsible for **all** defense questions of Projects I, II and III, not only the ones you answered in your videos. Your answers are taken into account in your project grades.

### Defense Questions

*Answer all questions in Section A and one question from each of Sections B–G in your video. In the final oral exam, you are responsible for all questions.*

#### A. Your Code and Results (all required)
1. Choose one line from your JSON cleaning/parsing code or your evaluation code (not an import, print or comment line). Explain what it does and show what happens when it is removed.
2. Did your AI assistant suggest anything that you decided not to use? Why not?
3. Which of your results surprised you? How do you explain it?
4. Explain the difference between the results you obtained with and without the `format` parameter.

#### B. Language Models and Attention
5. Explain how the model selects the next token, using the difference between an n-gram model and a Transformer.
6. How does the response time change as you add few-shot examples and make the prompt longer? Explain this using attention.

#### C. Generation Parameters
7. How do JSON parsing success and accuracy change if you increase the temperature?
8. With temperature set to 0, does the same prompt give the same result twice? If not, why?
9. Is there a difference between Top-K = 1 and temperature = 0? What happens when Top-K and Top-P are used together?
10. Which parameter would you change to increase parsing success, and why?

#### D. Quantization and Hardware
11. What is the quantization level of the model you used? How did you find out?
12. What differences in memory, speed and accuracy do you expect between the 4-bit, 5-bit, 8-bit and 16-bit versions of the same model (e.g., `Q4_K_M`, `Q5_K_M`, `Q8_0`, `F16`)? Which one did you choose for your own computer, and why? Compare at least two versions and show the results.
13. Approximately how many GB does the 4-bit version of a 7B-parameter model take? Show your calculation.
14. How would your results change if you used a smaller (1B) or a larger (8B) model?
15. What does Ollama do if the model does not fit into GPU memory? How does this affect speed? How can you check this on your own computer?

#### E. Tokenization
16. Why does the Turkish version of a text contain more tokens than its English version?
17. How does your model's tokenizer split the word "kitaplarımızdan"? Show it. (Ollama does not currently show how a text is split into tokens. Use the Hugging Face tokenizer of the same base model, e.g., `AutoTokenizer.from_pretrained("Qwen/Qwen2.5-7B-Instruct")`. Ollama's `prompt_eval_count` field gives only the number of tokens.)

#### F. Prompt Strategies: "What if we had tried…?"
18. How would your results change if you used 3-shot prompting instead of zero-shot? How would you select the examples?
19. Does changing the order of the few-shot examples change the result?
20. What would the model do if you deliberately gave wrong labels in the examples?
21. Would the result change if you wrote the prompt in English instead of Turkish, even though the data is Turkish?
22. How would accuracy and parsing success change if you asked the model to write its reasoning first and then produce the JSON?
23. Optimizing the system prompt directly affects success. How would you optimize your system prompt? Which changes would you try, and which metric would you use to measure success? On which data would you run these trials, and why should you not run them on the test data?

#### G. Comparison with Classical Methods
24. If you performed the same classification with TF-IDF and logistic regression, would it beat the LLM? In which case would it?
25. If you had only 10 labeled examples, which method would perform better: a classical model or a few-shot LLM?
26. If your classical model used plain word counts (BoW) instead of TF-IDF, would the result change? Which words would cause this difference?

Good luck.
