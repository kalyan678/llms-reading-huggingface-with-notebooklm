# LLMs Reading LLMs: Exploring Hugging Face Models with NotebookLM

This project explores how [Google’s NotebookLM](https://notebooklm.google.com/notebook/e5fc39aa-6d61-428f-b2be-951efd083175), an AI-powered research assistant, can be used to interactively question and analyze model documentation from Hugging Face’s Transformers library.

I uploaded multiple model cards (such as FLAN-T5, DistilBERT, and GPT-2) into NotebookLM and asked it a series of technical, comparative, and ethical questions. This unique setup allows us to evaluate how a document-grounded LLM assistant interprets real-world model documentation without hallucination.


## Objective

- Use NotebookLM to explore the reasoning, factual accuracy, and limitations of well-known Hugging Face models.
- Assess how grounded language models respond to prompts using only provided documentation.
- Identify risks like hallucination, bias, or gaps in documentation-based answers.

---

## Methodology

1. Selected 3 popular model cards: `flan-t5`, `gpt-2`, and `distilbert-base-uncased`.
2. Uploaded model documentation into a new NotebookLM notebook.
3. Asked curated questions about:
   - Model behavior (e.g., summarization)
   - Factual generation and hallucination risk
   - Comparison between models
   - Documentation gaps
4. Collected screenshots and generated answers.

---

## Sample Prompts

> Why did Hugging Face include GPT-2 despite its known risks?

> Why might a developer still choose BERT over newer models like FLAN-T5?

> Why can’t NotebookLM provide details about GPT-4.1?

> Based solely on the uploaded source documents, which model is more reliable for factual tasks?


All prompts are categorized in the [NotebookLm_Prompts.txt](./NotebookLm_Prompts.txt) file.

---

## Screenshots

### Summary Response Example
![Summary Response](https://github.com/kalyan678/llms-reading-huggingface-with-notebooklm/raw/main/Screenshot_1.png)

### Hallucination Prompt Result
![Hallucination Prompt](https://github.com/kalyan678/llms-reading-huggingface-with-notebooklm/raw/main/Screenshot_3.png)


---

## Key Takeaways

- NotebookLM can offer grounded and coherent summaries **only if the input sources contain the required information**.
- It performs well in *intra-document inference*, but fails when asked about *external models (e.g., GPT-4.1)* not present in the sources.
- Model documentation varies in completeness, affecting response quality.

---

## Folder Structure
```
llms-reading-llms/
├── README.md
├── LICENSE
├── Notebooklm_prompts.txt
├── models_info/
│ ├── flan-t5-summary.md
│ ├── gpt-2-card.txt
├── screenshots/
│ ├── summary-response.png
│ ├── comparison-question.png

```
