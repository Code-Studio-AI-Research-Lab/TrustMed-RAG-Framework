# TrustMed-RAG: A Verification-Driven Retrieval-Augmented Generation Framework for Trustworthy Medical Decision Support

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Framework: PyTorch / LangChain](https://img.shields.io/badge/Framework-PyTorch%20%2F%20LangChain-orange.svg)](https://pytorch.org/)
[![Domain: Trustworthy Healthcare AI](https://img.shields.io/badge/Domain-Medical%20RAG--XAI-red.svg)]()

This repository contains the official implementation of **TrustMed-RAG**, an advanced Retrieval-Augmented Generation (RAG) framework tailored specifically for high-stakes clinical decision support. Unlike standard RAG pipelines that blindly trust retrieved snippets, TrustMed-RAG introduces a rigorous, multi-stage **Verification-Driven Architecture**. It mathematically cross-checks retrieved clinical knowledge and generated medical advice against verified medical gold-standards (e.g., PubMed, clinical guidelines) to systematically eliminate hallucinations and provide mathematically sound, auditable provenance for clinicians.

---

## 📌 Research Vision & Core Concept
When standard LLMs use RAG for medical queries, they often suffer from *source conflict*, *irrelevant retrieval*, or *synthesis hallucination*. If a model synthesizes wrong dosage information, the consequences are critical. TrustMed-RAG solves this by implementing a dual-stage verification engine:
1.  **Retrieval Verification (Is the source correct?):** Evaluates whether the fetched documents from the vector database are contextually sound, up-to-date, and free of contradictions.
2.  **Generation Verification (Is the answer faithful?):** Probes the generated response against the retrieved source material using natural language inference (NLI) to ensure no ungrounded claims are made.



---

## 🛠️ Key Features & Methodology
1. **Dynamic Verification Engine:** Implements customized NLI (Natural Language Inference) models and cross-encoders to measure semantic entailment between questions, sources, and answers.
2. **Clinical Vector Store Pipeline:** Pre-configured architectures using Qdrant/FAISS vectorized over open medical repositories like PubMed Central and specialized clinical textbooks.
3. **Self-Correction Feedback Loop:** If a generated answer fails the verification threshold, the framework automatically triggers a re-querying or re-generation cycle.
4. **Fidelity-Latency Tradeoff Evaluation:** Tools to benchmark the rigorousness of verification checks against real-time operational inference speeds.

---

## 📂 Repository Structure
```text
├── src/
│   ├── ingestion/          # Data parsing, chunking, and medical vector store indexing
│   ├── retrieval/          # Semantic search, re-ranking, and source conflict detection
│   ├── verification/       # Dual-stage verification models (NLI hooks, source cross-encoders)
│   └── generation/         # Self-correcting generation loops and prompt orchestrators
├── data/                   # Benchmark loaders for MedQA, PubMedQA, and BioASQ
├── configs/                # Vector dimensions, similarity metrics, and verification thresholds
├── notebooks/              # Citation mapping graphs, hallucination tracking, and error analysis
├── Literature_Review/      # Team research matrices and BibTeX reference files
└── README.md
