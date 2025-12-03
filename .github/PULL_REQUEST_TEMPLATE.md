# Pull Request Checklist & Review Guide

This template ensures high-velocity, zero-defect integration. Please review and complete all relevant sections before submitting.

---

## 🚀 Feature / Fix Summary

<!-- Briefly describe the scope of this Pull Request. What does it accomplish? -->

**Related Issue(s):** (e.g., Closes #123, Fixes #456)

## ✅ Checklist (Developer)

*   [ ] **Architectural Alignment:** Does this adhere to the FSD/Modular Monolith principles (as defined in `AGENTS.md`)?
*   [ ] **Code Style:** Have I run the linter/formatter (`npm run lint` or equivalent)?
*   [ ] **Unit Tests:** Have I written/updated unit tests (`Vitest`/`Pytest`) for new or modified logic?
*   [ ] **E2E Tests:** If user-facing changes, have I updated Playwright/Cypress scenarios?
*   [ ] **Documentation:** Are relevant sections of `README.md` or inline comments updated?
*   [ ] **Performance:** Have I considered potential performance impacts (especially regarding AI/TTS latency)?
*   [ ] **Security:** Are all external API calls (Gemini) secured and validated? No hardcoded secrets?

## 🔬 Technical Deep Dive & Verification

<!-- Provide context for the reviewer. What major changes were made? Why? -->

### Architecture/Pattern Applied

> **Example:** Refactored TTS module into its own dedicated feature slice to adhere to Feature-Sliced Design principles, isolating browser API interactions from core processing logic.

### Testing Strategy

<!-- Detail how you verified the change. If you skipped E2E tests for a reason, document it here. -->

## 📋 Reviewer Checklist (For Reviewer Only)

*   [ ] **Correctness:** Does the implementation meet the requirement?
*   [ ] **Readability:** Is the code clean, idiomatic, and well-commented?
*   [ ] **Security Audit:** Are inputs sanitized? Are secrets handled correctly?
*   [ ] **Badge Compliance:** Are the changes reflected in the expected CI/CD outcomes?
*   [ ] **Documentation:** Is the system operating manual (README) accurate?

**Reviewer Notes:**

---

*This repository operates under the Apex Technical Authority standard. Submissions must aim for future-proof, zero-defect quality.*