# 📌 AI Solutions Trade-offs Evaluation

## Introduction

As part of the AI-driven certification enhancement initiative, our architectural committee conducted an in-depth trade-off analysis to determine the most effective approach to automating the grading and feedback processes. This phase involved:
- Identifying key challenges within the certification workflow.
- Brainstorming multiple AI-driven proposals.
- Evaluating each approach based on scalability, accuracy, operational cost, and explainability.

Before selecting the Auto Grading System for Test 1 and AI Feedback Assistant, several alternative solutions were analyzed. The following sections document these trade-offs, including additional approaches that were considered.

---

## 🔎 Trade-offs for Core Challenges

### 1️⃣ Grading Short-Answer Questions (Test 1)
**Objective:** Improve efficiency, accuracy, and scalability of short-answer grading.

| Approach | Pros | Cons |
|----------|------|------|
| Fully manual grading | Complete human control and high accuracy. | Time-intensive, costly ($50/hour per expert), does not scale. |
| Rule-based keyword scoring | Simple and explainable model.<br>Easy to implement. | Limited flexibility.<br>Fails on nuanced responses.<br>High false negatives. |
| Pattern-based NLP scoring | More flexible than keyword scoring.<br>Handles synonyms and rephrased answers. | Requires extensive fine-tuning.<br>Still lacks deep contextual understanding. |
| AI-generated scoring with human validation | Provides automation while ensuring accuracy. | Requires human resources for verification.<br>Not fully automated. |
| Blockchain-based grading transparency | Ensures immutability and traceability of scores.<br>Prevents tampering. | High implementation complexity.<br>Not directly related to grading logic. |
| Semi-automated rubric-based scoring | AI-assisted grading based on predefined rubrics. | Limited adaptability.<br>Requires frequent updates to rubric models. |
| Machine learning model trained on past grading decisions | Can learn from historical grading patterns. | Requires large datasets for training.<br>Potential bias in historical data. |
| Hybrid AI-assisted grading (✅ chosen) | Reduces expert workload.<br>Balances automation and human oversight.<br>Scales efficiently. | Requires initial training & fine-tuning.<br>Ongoing model validation. |
| Crowdsourced grading (peer review) | Distributed workload.<br>Reduces cost per submission. | Lacks standardization.<br>Requires additional verification layers. |

**Decision:** A hybrid AI-assisted approach was chosen as it provides the best balance between scalability, trust, and cost-efficiency, while keeping human evaluators involved in edge cases.

---

### 2️⃣ Generating Feedback for Candidates
**Objective:** Improve consistency, quality, and efficiency of feedback delivery.

| Approach | Pros | Cons |
|----------|------|------|
| Manual feedback from experts | Fully controlled.<br>Highly personalized. | Time-consuming.<br>Inconsistent quality.<br>Expert fatigue. |
| Predefined feedback templates | Fast implementation.<br>Standardized responses. | Lacks personalization.<br>Limited adaptability. |
| AI-generated feedback (✅ chosen) | Ensures structured, professional feedback.<br>Reduces expert workload.<br>Customizable system behavior. | Needs fine-tuning.<br>Requires expert validation. |
| Feedback synthesis using retrieval-augmented generation (RAG) | Generates feedback using a knowledge base of previous feedback examples. | Requires extensive database of past feedback.<br>Potential hallucination of responses. |
| Self-assessment with AI guidance | Encourages candidate reflection and learning. | May not align with certification standards.<br>High risk of misinterpretation by candidates. |

**Decision:** AI-generated feedback improves efficiency and standardization while keeping experts in control to validate and refine outputs.

---

### 3️⃣ AI Deployment Strategy
**Objective:** Determine the best approach for hosting AI models.

| Approach | Pros | Cons |
|----------|------|------|
| On-premise deployment | Full data control.<br>Works without external dependencies. | High infrastructure costs.<br>Scalability limitations.<br>Requires dedicated maintenance. |
| Cloud-based AI processing (✅ chosen) | Highly scalable.<br>Lower upfront costs.<br>Fast updates. | Requires compliance with cloud security policies.<br>Possible latency issues. |
| Edge computing AI | Reduces reliance on cloud.<br>Optimizes response times. | Requires complex deployment.<br>Higher hardware investment. |
| Federated learning for AI grading | Ensures privacy by keeping candidate data decentralized. | Complex to implement.<br>Requires synchronization of multiple AI models. |

**Decision:** Cloud deployment was selected to ensure scalability and cost-efficiency while maintaining security compliance.

---

### 4️⃣ Model Selection for Grading System
**Objective:** Identify the best AI model for evaluating short-answer responses.

| Model | Pros | Cons |
|-------|------|------|
| LLaMA 3 7B | High accuracy.<br>Handles complex queries. | Requires high computational power.<br>Higher inference costs. |
| Mistral 7B | Optimized for speed.<br>Less compute-intensive. | Less accurate for nuanced answers. |
| Phi-2 (✅ chosen) | Lightweight model.<br>Low infrastructure cost. | Limited reasoning ability.<br>May require model updates over time. |
| Fine-tuned BERT model | Customizable to specific grading needs. | Requires extensive training data.<br>Higher maintenance overhead. |
| GPT-4 Turbo | High generalization ability.<br>Fast inference. | Higher cost per API call.<br>May require additional filtering. |
| Zero-shot grading model with embeddings | Works without labeled training data.<br>Flexible across question types. | Less precise without fine-tuning.<br>Struggles with complex reasoning. |

**Decision:** Phi-2 was selected as a cost-efficient baseline, with the option to transition to LLaMA 3 if performance improvements are needed.

---

### 5️⃣ Feedback AI Model Selection
**Objective:** Identify the best AI model for restructuring and formatting feedback.

| Model | Pros | Cons |
|-------|------|------|
| Claude 3 Opus | High reasoning power.<br>200K+ context window. | Cloud-only solution.<br>Higher cost. |
| GPT-4 Turbo (✅ chosen) | Cost-effective.<br>Good balance between performance and cost. | 128K context window (lower than Claude 3). |
| LLaMA 3 / Deepseek R1 | Cheapest option.<br>Fine-tunable. | Requires extensive model customization.<br>Inferior language processing. |
| Custom-built Transformer Model | Can be fully tailored to certification feedback needs. | High cost and complexity.<br>Long development cycle. |
| Fine-tuned GPT-J model | Open-source and customizable. | Requires significant computational resources.<br>May lag behind in contextual accuracy. |
| Reinforcement learning-based feedback system | Trains the model iteratively based on user feedback. | Long training time.<br>High risk of feedback loops. |

**Decision:** GPT-4 Turbo was selected due to its strong NLP capabilities while being cost-effective for real-time feedback formatting.

---

## 🎯 Justification for Final Selections

Our architectural committee conducted a thorough evaluation of various AI-driven approaches to ensure that the proposed
solutions meet the scalability, cost-efficiency, and accuracy requirements of the certification process.
The chosen solutions were selected based on their ability to balance automation with human oversight, ensuring that
grading remains trustworthy, explainable, and adaptable to changing certification standards. By integrating AI in a
controlled, hybrid manner, we establish a foundation that enhances efficiency without compromising reliability.
This approach also allows for future optimizations, such as adaptive learning models and more in-depth analytics-driven assessments.

| Decision Area | Chosen Approach | Key Benefit |
|--------------|----------------|-------------|
| Grading Approach | Hybrid AI-assisted grading | Balances scalability, cost-efficiency, and expert validation. |
| Feedback Generation | AI-generated structured feedback | Improves feedback consistency while keeping expert oversight. |
| Deployment Strategy | Cloud-based AI | Ensures scalability with lower infrastructure costs. |
| Grading Model | Phi-2 | Cost-efficient and fast, with an option to scale up. |
| Feedback Model | GPT-4 Turbo | Optimal balance between cost and performance. |
