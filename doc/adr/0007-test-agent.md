# 📜 ADR 007: Test Agent

**Date:** 2025-02-16  
**Classification:** Feature

---

## 📌 Context

Currently, we can automate the reviewing process via the [Test Agent](0001-test-agent.md) only for the Test 1 part  
But when the [Unified Testing Platform](0006-unified-testing-platform.md) is implemented, we can extend our agent to allow it to test the Test 2 part as well

---

## 🎯 Decision

- The agent needs to be trained on the existing database of exam results
- Diagrams have to be parsed in an understandable format like JSON by the AI agent
- The agent has to analyze a submitted solution
- It has to rank the score with primitive values such as low, medium, high after analyzing a submitted result
- The agent decides if it should send the result to a person who can check it by hand or not based on the score

---

## ⚖️ Consequences

- The service's quality is improved
- The experts and companies trust the certification center because they know the results are accurate
- Reducing reviewing time and cost savings by delegating human responsibilities to the agent
- AI agent could be used for potential new features such as:
    - [Anti-Plagiarism Agent](0008-anti-plagiarism-agent.md)  
