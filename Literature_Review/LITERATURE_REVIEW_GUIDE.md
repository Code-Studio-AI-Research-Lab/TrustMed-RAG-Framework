# 📊 Onboarding Guide: Literature Review & Research Matrix for TrustMed-RAG

Welcome to the **Code Studio AI Research Lab**. This guide establishes the mandatory workflow, literature logging standards, and Git guidelines for all team members working on our project: **"TrustMed-RAG: A Verification-Driven Retrieval-Augmented Generation Framework for Trustworthy Medical Decision Support"**.

---

## 🔍 1. Where to Find High-Impact Papers
Retrieval-Augmented Generation (RAG) and LLM hallucination mitigation are among the fastest-evolving fields in AI. To build a trustworthy clinical framework, look for papers exclusively in these elite venues:
* **Google Scholar:** [scholar.google.com](https://scholar.google.com/) (Filter: *Since 2024* or *2025* for cutting-edge self-correction and RAG verification loops).
* **Top AI/NLP Conferences:** **ACL**, **EMNLP**, **NAACL**, **ICLR**, and **NeurIPS**.
* **Medical AI Venues:** **MICCAI**, **BioNLP Workshop**, and high-impact biomedical informatics journals like *JAMIA*.
* **OpenReview:** [openreview.net](https://openreview.net/) (Excellent for checking active peer-reviews and criticisms of new RAG architectures).

---

## 🛠️ 2. Advanced Search Queries & Operators
Do not search using broad terms. Use precise **Boolean Operators** (`AND`, `OR`, `""`) to filter down to verification-driven architectures:
* **Core RAG Query:** `"Retrieval-Augmented Generation" AND "Medical Decision Support" AND "Hallucination"`
* **Verification Query:** `"Natural Language Inference" AND "Factual Verification" AND ("RAG" OR "Retrieval")`
* **Self-Correction Query:** `"Self-correction loop" AND "Large Language Models" AND "Clinical Accuracy"`

---

## 📖 3. How to Read & Critically Evaluate a RAG Paper
When reading papers on medical knowledge retrieval, focus heavily on the mathematical and logical boundaries enforced on the model. Use the **Three-Pass Method** and answer:
1.  **The Verification Metric:** How do the authors verify the output? Did they use an independent, deterministic metric (like NLI/Cross-Encoders), or did they simply ask a larger model like GPT-4, *"Is this answer correct?"* (Beware: LLM-as-a-judge can also hallucinate).
2.  **Document Chunking & Vectorization:** Look at their data ingestion layer. Did they chunk medical text by fixed token sizes, or did they use semantic/sentence-level overlapping? Chunking directly impacts verification accuracy.
3.  **The Inefficiency Flaw (Our Opportunity):** Check their **Limitations** section. Does their verification or self-correction loop slow down the system too much? *Our core research gap is optimizing the fidelity-latency tradeoff so doctors can use it in real-time.*

---

## 📊 4. Maintaining the Central Research Matrix Table
Every paper you read must be logged immediately into `Literature_Review/Research_Matrix.md`. This table ensures our collective lab avoids duplicate efforts and identifies technical gaps instantly.

### The Matrix Format:
| Citation & Venue | Retrieval Source | Specific Verification Mechanism | Core Evaluation Benchmark | Key Performance Metrics | Found Limitations & Gaps (Our Opportunity) | Reviewer Name |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| *e.g., Gao et al., 2024 (ACL)* | General text/Wikipedia | Overview of simple retrieval vs generation checks. | General QA | Classified RAG models into Advanced and Modular branches. | Focused entirely on general knowledge; did not address high-stakes medical constraints where a single citation mismatch breaks clinical safety. | Rahim |
| **[Your Entry]** | | | | | | Your Name |

### How to add your entry:
1. Open `Literature_Review/Research_Matrix.md` in your text/code editor.
2. Scroll to the bottom of the table and add a new row using pipe (`|`) boundaries.
