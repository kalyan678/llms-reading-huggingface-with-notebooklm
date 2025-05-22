
# Hugging Face Model Cards & Fine-Tuning Guide

---

## 🔹 Model 1: BERT (Bidirectional Encoder Representations from Transformers)

- **Author**: Google AI Language
- **Link**: https://huggingface.co/bert-base-uncased
- **Use Cases**: Named Entity Recognition, Sentiment Analysis, Q&A
- **Parameters**: 110M
- **Architecture**: Transformer encoder
- **Fine-Tuning Tip**: Use [CLS] token representation for classification tasks.

---

## 🔹 Model 2: DistilBERT

- **Author**: Hugging Face
- **Link**: https://huggingface.co/distilbert-base-uncased
- **Use Cases**: Similar to BERT but more efficient
- **Parameters**: 66M
- **Speed**: 60% faster than BERT with 97% of its performance
- **Fine-Tuning Tip**: Great for low-latency environments like mobile or browser-based apps.

---

## 🔹 Model 3: GPT-2

- **Author**: OpenAI
- **Link**: https://huggingface.co/gpt2
- **Use Cases**: Text Generation, Chatbots
- **Parameters**: 124M (base model)
- **Architecture**: Transformer decoder
- **Fine-Tuning Tip**: Train with causal language modeling (next token prediction).

---

## 🔹 Model 4: FLAN-T5 (Instruction-Tuned T5)

- **Author**: Google
- **Link**: https://huggingface.co/google/flan-t5-base
- **Use Cases**: Summarization, Translation, Q&A
- **Parameters**: 250M
- **Key Feature**: Instruction tuning — works better with natural instructions
- **Fine-Tuning Tip**: Use Seq2SeqTrainer with datasets like XSum or CNN/DailyMail.

---

## 📘 Fine-Tuning Summary (General Steps)

1. Load pre-trained model & tokenizer from Hugging Face
2. Preprocess your dataset using `datasets` and `transformers` libraries
3. Define training arguments (batch size, learning rate, epochs)
4. Use `Trainer` or `Seq2SeqTrainer` API to train
5. Save the model and tokenizer
6. Evaluate on custom test set using metrics (F1, BLEU, ROUGE)

---

## 🧠 Useful Metrics

- **Accuracy**: Simple classification score
- **F1 Score**: Balances precision and recall
- **BLEU / ROUGE**: Translation/summarization evaluation
- **Perplexity**: Language modeling fluency

---

## 🔗 Tools & Libraries

- `transformers`
- `datasets`
- `evaluate`
- `accelerate` (for distributed training)
- `PEFT` (for parameter-efficient fine-tuning like LoRA)

---

## ✅ Next Steps

Ask questions like:
- "Which model is best for summarizing legal documents?"
- "How can I fine-tune GPT-2 with 1000 examples?"
- "Compare BERT and DistilBERT in terms of speed and size."

---
