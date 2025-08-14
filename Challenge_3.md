Assignment: Courtroom Clash – AI Lawyers Battle It Out! 🤖⚖️🔥
Objective
In this assignment, you will develop an interactive AI-powered legal debate system where two AI chatbots—one using RAG (Retrieval-Augmented Generation) for factual legal arguments and the other relying on pure improvisation and loophole nonsense—face off in a courtroom-style battle.
You will build a backend for argument generation, implement hybrid retrieval techniques with effective metadata usage, and create a simple interactive frontend where users play the role of Judge, deciding which AI wins each case.
Key Features to Implement
1. AI Roles
RAG Lawyer (Prosecution): Uses hybrid retrieval techniques and structured metadata storage to generate fact-based legal arguments from a small dataset of legal cases, precedents, and laws.
Chaos Lawyer (Defense): Uses a fully generative model that does not rely on retrieval, instead crafting absurd, exaggerated, or completely fictional counterarguments.
User (Judge): Watches the debate and decides the winner—or introduces random events that change the course of the trial.

2. Metadata Usage for RAG Lawyer
RAG Lawyer should retrieve and rank legal cases effectively by storing and utilizing metadata for improved relevance. Some useful metadata fields include:
Case Type (e.g., defamation, property dispute, criminal case)
Jurisdiction (e.g., US, UK, EU law)
Year of Judgment (e.g., 1994, 2020)
Key Legal Principles (e.g., burden of proof, contract law, negligence)
Plaintiff/Defendant Details (e.g., corporation vs. individual, government vs. private entity)
Case Outcome (e.g., dismissed, settled, guilty, acquitted)
Hybrid Retrieval Strategy
Keyword Retrieval
Semantic Retrieval
Metadata filtering and ranking: Once retrieved, cases should be filtered and ranked using stored metadata. Example:
If the case involves defamation, prioritize cases where "Key Legal Principles" include "libel/slander."
If the user’s case involves a corporate entity, prioritize legal precedents where "Plaintiff/Defendant Details" match.
Example metadata-enhanced retrieval query:
{
  "query": "Can a parrot be sued for defamation?",
  "filters": {
    "case_type": "defamation",
    "jurisdiction": "US",
    "year_range": "2000-2023"
  },
  "retrieval_method": "hybrid"
}


Assignment Tasks
Task 1: Backend Implementation (FastAPI or Flask)
Implement an API that supports:
Generating random legal cases for debate (e.g., "A man sues a parrot for defamation.").
Retrieving legal facts and precedents using metadata-enhanced hybrid retrieval for RAG Lawyer.
Generating wild counterarguments for Chaos Lawyer.
Allowing the user (Judge) to pick a winner or introduce new evidence.
📌 Example API Endpoint:
POST /generate_case → Returns a new case scenario.
POST /debate → Starts a round between RAG and Chaos Lawyers.
POST /judge_decision → Accepts user input on the verdict.

Task 2: Structured Input and Output with Metadata
Define a structured input format where users provide case details (or generate random ones).
Ensure structured JSON output that organizes arguments and metadata-based retrieval.
Example:
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


Task 3: Frontend Implementation (React or Streamlit)
Design a simple UI where:
The user (Judge) picks a winner.
Display retrieved metadata, showing how RAG Lawyer selects relevant cases.

Note on Bonus Features
🚨 Important: Bonus features should only be implemented after the main system is fully functional. These additional features are not a priority in the final evaluation.
Optional Enhancements:
Objection Handling: Allow users to interrupt AI responses.
Lawyer Role Reversal: Swap AI lawyer roles to test adaptability.
Auto-Summarized Verdicts: Generate a courtroom-style ruling based on argument strength.

🔥 Get ready to see which AI lawyer wins the most ridiculous courtroom battles! 🚀
