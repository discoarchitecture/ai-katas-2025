# 📜 ADR 006: Unified Testing Platform

**Date:** 2025-02-16  
**Classification:** Killing feature & risky investment

---

## 📌 Context

Currently, a Test 2 result could be submitted in any available formats such as PDF, SVG, Drawio, etc  
It's almost impossible to analyze work using AI because it requires a lot of resources, training time and costs  
Even with AI, there's still a lot of risk for mistakes

---

## 🎯 Decision

- Implement a custom platform for diagram building
- Participants have to do and submit the result only within the platform
- Under the hood, the diagrams need to be converted to a common format like JSON

---

## ⚖️ Consequences

- The service's quality and candidates' experience are improved
- There's a huge potential for next features such as:
    - Security improvements
    - Unified results database for AI trainings
    - [Test Agent](0007-test-agent.md) for the Test 2 part
    - [Anti-Plagiarism Agent](0008-anti-plagiarism-agent.md)
- A lot of costs at first, but it could be very profitable in the long run  
