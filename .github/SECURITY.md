# Security Policy for ZenRead-AI-Reader-Mode-And-TTS-Browser-Extension

**Last Updated:** December 2025 (Apex Authority Standard)

## 1. APEX SECURITY MANDATE

This repository, `ZenRead-AI-Reader-Mode-And-TTS-Browser-Extension`, adheres to the **Apex Security Mandate**, emphasizing a proactive, zero-trust approach to software security. Our goal is to ensure the integrity, confidentiality, and availability of the extension and its users' data. We operate under the principle that security is not an afterthought but an integral part of the development lifecycle.

## 2. REPORTING SECURITY VULNERABILITIES

We encourage responsible disclosure of security vulnerabilities. If you discover a security issue, please follow these steps:

1.  **DISCOVER:** Identify a potential security vulnerability.
2.  **REPORT:** Submit a detailed report through one of the following secure channels:
    *   **GitHub Security Advisory:** Visit `https://github.com/chirag127/ZenRead-AI-Reader-Mode-And-TTS-Browser-Extension/security/advisories` to create a private security advisory.
    *   **Email (Encrypted):** For highly sensitive findings, use an encrypted email to `security@apex-architects.dev` (This is a placeholder for demonstration; in a real scenario, a dedicated, secure security email would be used).

**Your report should include:**
*   A clear and concise description of the vulnerability.
*   Steps to reproduce the vulnerability.
*   The potential impact of the vulnerability.
*   Any mitigation or remediation suggestions.
*   Proof-of-Concept (PoC) code, if applicable and safe to share.

## 3. OUR COMMITMENT

*   **Timely Response:** We will acknowledge your report within **48 hours** of receipt.
*   **Thorough Investigation:** We will investigate all valid reports promptly.
*   **Disclosure Plan:** Upon confirmation and resolution, we will coordinate a disclosure plan with you, respecting your contributions.
*   **No Reprisal:** We will not engage in legal action against individuals or groups who report vulnerabilities in good faith and adhere to this policy.

## 4. SECURITY BEST PRACTICES (LATE 2025 STANDARDS)

*   **Privacy-First Design:** As per the project's core principles, user privacy is paramount. No server-side processing, no tracking, and minimal local storage are employed. Data processed is ephemeral and strictly confined to the user's browser.
*   **Manifest V3 Compliance:** The extension is developed and maintained to comply with Manifest V3 standards, ensuring robust security controls and leveraging Chrome's (and compatible browsers') enhanced security features.
*   **Dependency Management:** All third-party dependencies are managed using `npm` and regularly scanned for known vulnerabilities using tools integrated into the CI pipeline (`npm audit`). Updates are prioritized based on severity.
*   **AI Model Security:** When interacting with AI models (e.g., Gemini API), utmost care is taken to sanitize inputs and outputs, preventing prompt injection or data leakage. API keys are managed securely via environment variables and are never committed to the repository.
*   **Code Integrity:** Linting and static analysis are enforced via `Biome` (or similar modern JS linters) and a strict CI/CD pipeline (`.github/workflows/ci.yml`) to catch potential security flaws early.
*   **Secure Storage:** Sensitive data (like API keys) is handled strictly through environment variables or secure browser storage mechanisms and is never hardcoded.

## 5. DEPENDABOT CONFIGURATION

Dependabot alerts are enabled for this repository to automatically detect and notify us of known vulnerabilities in dependencies. The CI pipeline includes automated checks to flag vulnerable packages.

## 6. LEGAL DISCLAIMER

This security policy is intended to guide security vulnerability reporting and does not constitute an agreement or offer of reward. All security work is performed on a volunteer basis by the project maintainers.

Thank you for helping keep `ZenRead-AI-Reader-Mode-And-TTS-Browser-Extension` secure!
