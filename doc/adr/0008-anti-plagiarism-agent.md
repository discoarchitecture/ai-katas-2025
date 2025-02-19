# 📜 ADR 008: Anti-Plagiarism Agent

**Date:** 2025-02-16  
**Classification:** Killing feature

---

## 📌 Context

[Analytics Agent context](0003-analytics-agent.md#context)

---

## 🎯 Decision

- Extend the [Analytics](0003-analytics-agent.md) and [Test](0007-test-agent.md)
- The agent needs to understand a chain logic and point out a submitted result with a similar one from the existing database
- Notify a human expert when the AI agent decides the work is "copy-pasted"
- Send a reference on the existing solution from the database

---

## ⚖️ Consequences

- The service's quality is improved
- The experts and companies trust the certification center because they know the results are accurate
- Detect companies from where employees try to cheat  
