# Challenge 2 — Domain Jargon Simplification

## Overview

In many professional fields — such as medicine, law, and technology — texts are filled with jargon that can be difficult for the general public to understand. This challenge is to design an AI system that can take jargon-heavy sentences and rewrite them into **plain, everyday English** while preserving their original meaning.

This task mirrors real-world applications in accessibility, public communication, and education, where clarity is essential without sacrificing accuracy.

---

## Task

Your goal is to build a system that:

1. **Identifies** complex or uncommon words and phrases in a sentence.
2. **Replaces** them with simpler, more common alternatives.
3. **Produces** a rewritten sentence that is easier for a layperson to understand while keeping the meaning intact.

---

## Dataset Creation

You will **create your own dataset** by collecting real-world jargon-heavy sentences from the internet.
Examples of sources:

* Medical research abstracts
* Legal documents
* Technical product manuals
* Academic articles in any field

Each row of your dataset should contain:

* **Original** — the jargon-heavy sentence
* **Simplified** — your rewritten plain-English version of that sentence

**Note:** Ensure the simplified version is **meaning-preserving** and free of grammatical errors.

---

## Submission Format

Your final submission must be a CSV file with the following format:

```
Original,Simplified
The cardiovascular examination revealed arrhythmia.,The heart check-up showed an irregular heartbeat.
The statute prohibits any such encroachment.,The law forbids such an intrusion.
```

**Requirements:**

* The CSV must include exactly **two columns**: `Original` and `Simplified`.
* All sentences must be in English.

---

## Evaluation Metric

Submissions will be evaluated using the **BLEU score**, which measures how closely your simplified sentences match the expected simplified versions.

---

## Deliverables

1. **Dataset** — Your own collected and simplified sentence pairs.
2. **Submission CSV** — With the `Original` and `Simplified` columns for the test set.
3. **Report (1–2 pages)** — Explaining your approach, data collection process, simplification strategy, and model design.

---

## Resources (to guide your understanding, not exact solutions)

* Research Paper: [Text Simplification via Paraphrasing](https://arxiv.org/abs/1906.05885)
* Research Paper: [A Neural Approach to Text Simplification](https://aclanthology.org/Q18-1042/)
* YouTube Video: [Text Simplification with NLP](https://youtu.be/0V96wE7lY4w?si=qsHZTSLiAOX41mAh)
