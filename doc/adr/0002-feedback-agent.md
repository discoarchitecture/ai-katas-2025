# 📜 ADR 002: Feedback Agent

**Date:** 2025-02-16  
**Classification:** Feature

---

## 📌 Context

Writing feedback takes a lot of time for each candidate who took an exam  
The more users we have, the faster our experts can give accurate and personalized feedback based on their answers and solutions

---

## 🎯 Decision

- A simple LLM (Large Language Model) is used to analyze the submitted result, detect knowledge gaps, and prepare general keys to highlight the strengths and weaknesses of the submitted solution
- **Important**: An AI agent doesn't have to generate fully automated feedback because it could hurt customer loyalty. It just has to make it easier for an expert to send feedback
- As a side feature, the agent can find and highlight an expert's voice tone to make it more polite and friendly

---

## ⚖️ Consequences

- By preparing the entry point for a human, we can reduce reviewing time and costs
- Improving loyalty by giving more personal feedback in shorter time  
