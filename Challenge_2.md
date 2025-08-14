## Challenge 2 — Domain Jargon Simplification

### Overview

Professional domains—such as medicine, law, and technology—often employ specialized jargon that poses a challenge for general audiences. In this challenge, you'll build an AI system capable of translating such jargon-heavy sentences into **clear, plain English**—retaining their original meaning.

This has real-world impact in areas like **education**, **legal transparency**, and **public communication**, where making complex ideas accessible is vital.

---

### Task

Design a **non–neural network** pipeline that:

1. **Identifies** complex or uncommon terms and phrases.
2. **Substitutes** them with simpler, more familiar alternatives.
3. **Produces** a rewritten sentence in plain English without changing the original meaning.

**Important Constraint:**
🚫 You **cannot** use deep learning or neural network–based models (e.g., BERT, GPT, LSTMs, Transformers).
✅ You **can** use:

* Classical machine learning models (e.g., decision trees, SVMs, Naive Bayes)
* Rule-based systems
* Dictionary/lexicon lookups (e.g., WordNet, custom synonym lists)
* Statistical techniques (e.g., frequency-based word substitution)

---

### Dataset Creation

You must create your own dataset, containing paired sentences:

* **Original**: the jargon-heavy source sentence.
* **Simplified**: the rewritten plain-English version.

**Requirements:**

* Cover at least **three distinct domains** (e.g., medicine, law, tech).
* Minimum **1,000 sentence pairs**.
* Stored as a CSV with exactly two headers:

  ```csv
  Original,Simplified
  ```

---

### Submission Format

Submit a CSV file named `submission.csv` containing your model’s simplified outputs on the test set:

```csv
Original,Simplified
The cardiovascular examination revealed arrhythmia.,The heart check-up showed an irregular heartbeat.
The statute prohibits such encroachment.,The law forbids such intrusion.
```

---

### Evaluation Metric

Your submission will be evaluated using the **BLEU** metric against reference simplifications.

---

### Resources

* **Research**: [SARI Metric for Text Simplification](https://nlpprogress.com/english/simplification.html) – Overview of text simplification metrics.

---

### Deliverables

1. **Dataset** (`dataset.csv`) – `Original,Simplified` pairs.
2. **`submission.csv`** – Simplified outputs for the test set.
3. **Approach Report (1–2 pages)** – Must describe:

   * Data collection method
   * Non-neural approach chosen and why
   * Challenges and lessons learned
