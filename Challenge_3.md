Here’s **Challenge 3** rewritten in the same **standard style** as Challenge 1 & 2 so it fits into your recruitment challenge set.

---

# Challenge 3 — Courtroom Clash: AI Lawyers Battle It Out! 🤖⚖️🔥

## Overview

In this challenge, you will build an **interactive AI-powered legal debate system** where two AI lawyers face off in a courtroom battle.

* **RAG Lawyer (Prosecution)** — Uses **Retrieval-Augmented Generation (RAG)** with hybrid retrieval and metadata filtering to produce **fact-based legal arguments** from a small dataset of legal cases, precedents, and laws.
* **Chaos Lawyer (Defense)** — Relies on **improvisation** and wild, often absurd arguments without retrieval, using creativity and loophole-based reasoning.
* **User (Judge)** — Observes the debate, chooses the winner, or introduces unexpected events that change the course of the trial.

This challenge blends **AI retrieval systems**, **metadata-based ranking**, and **creative language generation** with a **simple interactive UI**.

---

## Task

### 1. Backend (FastAPI or Flask)

Implement an API that supports:

* **Case Generation** — Randomly generate quirky legal scenarios (e.g., *"A man sues a parrot for defamation"*).
* **Metadata-Enhanced Retrieval** — For RAG Lawyer, use hybrid retrieval (keyword + semantic search) with metadata filtering.
* **Chaos Lawyer Response** — Generate absurd and exaggerated counterarguments without retrieval.
* **Judge Interaction** — Accept the Judge’s decision or allow them to introduce new evidence.

Example API endpoints:

```
POST /generate_case      → Returns a random or user-provided legal case scenario.  
POST /debate             → Generates arguments for both RAG and Chaos Lawyers.  
POST /judge_decision     → Records the Judge’s verdict or new evidence.  
```

---

### 2. Metadata Usage for RAG Lawyer

The RAG Lawyer must store and use metadata for improved case relevance. Suggested fields:

* **Case Type** — e.g., defamation, property dispute, criminal case
* **Jurisdiction** — e.g., US, UK, EU law
* **Year of Judgment** — e.g., 1994, 2020
* **Key Legal Principles** — e.g., burden of proof, contract law, negligence
* **Plaintiff/Defendant Details** — e.g., corporation vs. individual
* **Case Outcome** — e.g., dismissed, guilty, settled

**Hybrid Retrieval Flow:**

1. **Keyword Search**
2. **Semantic Search**
3. **Metadata Filtering & Ranking** — Example: For defamation cases, prioritize precedents where “Key Legal Principles” include libel/slander.

---

### 3. Structured Input & Output

The system should use JSON for input/output:

**Example Output:**

```json
{
  "case": "A man sues a parrot for defamation.",
  "rag_lawyer": {
    "argument": "Under defamation law, only humans can be sued for libel. A precedent from Smith v. Talking Pets (1994) confirms this.",
    "citation": "Smith v. Talking Pets, 1994",
    "metadata": {
      "case_type": "defamation",
      "jurisdiction": "US",
      "key_legal_principles": ["libel", "intent", "publication"],
      "outcome": "dismissed"
    }
  },
  "chaos_lawyer": {
    "argument": "Ah, but what if the parrot was *coached*? In the case of Polly v. Human Dignity (2005), a bird was declared an 'agent of slander'!",
    "rhetoric": "If a voicemail can be defamatory, why not a talking parrot?!"
  },
  "judge_decision": "Pending user input."
}
```

---

### 4. Frontend (React or Streamlit)

Create a simple interface where:

* The Judge (user) views both arguments.
* The Judge can **pick the winner** or introduce **random new events**.
* RAG Lawyer’s retrieved metadata is displayed alongside their argument.

---

## Deliverables

1. **Backend API** — Fully functional RAG + Chaos Lawyer debate generation.
2. **Frontend UI** — Judge interaction panel.
3. **Metadata Storage** — Used effectively in RAG retrieval.
4. **Report (1–2 pages)** — Explaining your approach, retrieval strategy, metadata structure, and system design.

---

## Evaluation

* **Functionality** — All required features work.
* **Metadata Use** — RAG retrieval improves case relevance.
* **Creativity** — Chaos Lawyer arguments are entertaining but still structured.
* **UI Usability** — Judge can easily control the debate.

---

## Bonus Features (Optional)

* **Objection Handling** — Allow users to interrupt AI responses.
* **Lawyer Role Reversal** — Swap AI roles to test adaptability.
* **Auto-Summarized Verdicts** — AI-generated courtroom-style rulings.

---

Do you want me to now **combine Challenge 1, 2, and 3** into a single polished **Recruitment Challenge PDF/README** so they all have the same structure and styling? That would make it easier for participants to follow.
