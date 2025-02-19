# 📜 ADR 001: Test Agent

**Date:** 2025-02-16  
**Classification:** Feature

---

## 📌 Context

The review process for submitted exams is the primary bottleneck in the business model. It could be improved by outsourcing the process to an AI agent

While Test 2 requires more complicated logic, we can speed up and automate the process for Test 1

---

## 🎯 Decision

- The agent needs to be trained on the existing database of exam results
- While ABC answers can be checked by code, answers that have been manually typed have to be checked by the agent
- It has to rank the score with primitive values such as low, medium, high after analyzing a submitted result
- The agent decides if it should send the result to a person who can check it by hand or not based on the score

---

## ⚖️ Consequences

- The service's quality is improved
- The experts and companies trust the certification center because they know the results are accurate
- Reducing reviewing time and cost savings by delegating human responsibilities to the agent  
