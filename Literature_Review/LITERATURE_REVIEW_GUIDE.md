# 📊 Onboarding Guide: Literature Review Workflow for TrustMed-RAG

Welcome to the **Code Studio AI Research Lab**. This guide establishes the mandatory workflow for conducting the Literature Review for our project: **"TrustMed-RAG: A Verification-Driven Retrieval-Augmented Generation Framework for Trustworthy Medical Decision Support"**.

---

## 🔍 1. Where to Find High-Impact Papers
RAG frameworks and LLM evaluation are currently some of the fastest-evolving fields in AI. Search for papers in these elite venues:
* **Top AI/NLP Conferences:** **ACL**, **EMNLP**, **NAACL**, **ICLR**, and **NeurIPS**.
* **Medical AI Venues:** **MICCAI**, **BioNLP Workshop**, and *AMIA Joint Summits on Translational Science*.
* **Open Platforms:** Google Scholar, arXiv, and OpenReview (specifically inspect ICLR submissions regarding "Self-Correction" or "RAG Hallucinations").

---

## 🛠️ 2. Search Strategy & Keywords
Since we focus strictly on verification and trustworthiness, use targeted search strings:
* **Query 1:** `"Retrieval-Augmented Generation" AND "Medical Decision Support" AND "Hallucination"`
* **Query 2:** `"Natural Language Inference" AND "Factual Verification" AND "RAG"`
* **Query 3:** `"Self-correction loop" AND "Large Language Models" AND "Clinical Accuracy"`

---

## 📖 3. How to Read & Critically Evaluate a RAG Paper
1. **Analyze the Verification Metric:** Did the authors verify the text using an independent scoring metric, or did they simply ask a large model like GPT-4, *"Is this answer correct?"* (GPT-4 evaluation can itself hallucinate!).
2. **Examine the Dataset Complexity:** Did they test on simple multiple-choice questions (e.g., MedQA) or complex, messy, free-text electronic medical logs?
3. **Identify the Inefficiency Flaw:** Look at their **Limitations**. Does their verification loop slow down the system so much that it's too slow for a doctor to use in real-time? *Our opportunity is optimizing the fidelity-latency tradeoff.*

---

## 📂 4. GitHub Directory Management Rules
```text
TrustMed-RAG-Framework/
└── Literature_Review/
    ├── PDFs/                 # Store paper PDFs (Format: FirstAuthor_Year.pdf, e.g., Gao_2024.pdf)
    ├── BibTeX/               # Append raw BibTeX blocks to `citations.bib`
    └── Research_Matrix.md    # Update the markdown matrix table
