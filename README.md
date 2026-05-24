# ALIA — Multi-Agent Medical Sales Simulator

**Agentic AI platform for pharma training · Real-time compliance enforcement · Stress analysis**

🎬 **[Watch the Live Demo on LinkedIn](https://www.linkedin.com/posts/latiri-eya-6ba97a292_integratedproject-agenticai-pharmainnovation-ugcPost-7459367135052550145-GpO8)**

---

## 🔒 NDA Notice

Source code and architecture are proprietary — developed under a confidentiality agreement with **Vital Tunisia**. This README covers the problem, design decisions, and measured results only. [Reach out on LinkedIn](https://www.linkedin.com/in/latiri-eya-6ba97a292) for further discussion.

---

## The Problem

Medical sales reps train theoretically — they never practice against realistic doctor profiles or real objections before entering the field. Meanwhile, healthcare professionals in remote areas need compliant, on-demand product information that a human rep can't always deliver. ALIA solves both with a single platform.

---

## Two Modes

**Mode 1 — Training & Simulation**
A rep selects a scenario, specialty, and difficulty level. The system generates a physician persona and runs a full simulated medical visit via voice or text. Every AI response is compliance-validated before delivery. The session ends with a performance score, structured feedback, and a revision sheet.

**Mode 2 — Medical Presentation**
A physician interacts directly with a virtual medical delegate — asking questions, requesting product details — and receives compliant, retrieval-grounded answers in real time. No appointment, no rep availability required.

---

## Why Agentic AI — Not Just a Generative Model

A single prompted LLM cannot guarantee compliance in a regulated industry — prompt instructions drift under adversarial input. ALIA uses a network of specialized agents, each with a single bounded responsibility: dialogue, scenario generation, compliance validation, and performance evaluation. Compliance is a hard gate enforced at the system level, not a prompt instruction a model can ignore. This is the core architectural reason for choosing agentic AI over a standard generative pipeline — and why LangGraph, which supports stateful graphs, conditional routing, and native cyclic flows (needed for the compliance retry loop), was selected over linear frameworks like CrewAI.

---

## Tech Stack

| Layer | Stack |
|---|---|
| Frontend | React, Three.js, WebRTC |
| Backend | FastAPI, Python |
| Orchestration | LangGraph |
| Language Models | Fine-tuned LLM · Shared LLM · Compliance LLM · Encoder–Decoder LLM |
| Retrieval | MiniLM-L12-v2, FAISS |
| Speech | OpenAI Whisper, VAD |
| Stress Analysis | OpenSMILE · rPPG · custom fusion model |
| Vision | OCR model for product detection |
| Analytics | CRM dashboard — compliance, stress timeline, evaluator scores |

---

## Results

**LangGraph Pipeline**

| Metric | Result |
|---|---|
| Node Execution Coverage | **100%** |
| Routing Consistency | **OK** |
| State Stability | **STABLE** |
| Graph Complexity Utilization | **5 / 5** |

**RAG Retrieval**

| Metric | Result |
|---|---|
| Chunk Retrieval Coverage | **100%** |
| RAG Family Hit Rate | **3 / 3** — scenario ✓ · difficulty ✓ · process ✓ |
| Difficulty Context Completeness | **100%** |
| Context Faithfulness | **100%** — 0 unsupported product claims |
| Scenario Relevance Score (cosine) | **0.354** — below 0.55 target; domain-adapted embeddings identified as fix |

**Fine-Tuning Impact — Scenario Agent**

| Metric | Base LLM | + Fine-Tuned | Delta |
|---|---|---|---|
| Profile generation success | 0% | **70%** | **+70pp** |
| RAG–FT difficulty merge | 30% | **100%** | **+70pp** |
| Context utilisation | 40% | **60%** | **+20pp** |

Fine-tuning is what makes simulation mode work — profile generation fails entirely without it.

---

## Screenshots
Training and simulation interface with real-time stress analysis:

<img width="548" height="257" alt="image" src="https://github.com/user-attachments/assets/3c855349-4a25-403e-820a-85e1b3030ca1" />


Expert interface for product and interaction with ALIA:


<img width="544" height="257" alt="image" src="https://github.com/user-attachments/assets/b69f6f4d-8952-4ec2-8dbf-fdaf63ce503e" />



---

*[Eya Latiri](https://www.linkedin.com/in/latiri-eya-6ba97a292)*
