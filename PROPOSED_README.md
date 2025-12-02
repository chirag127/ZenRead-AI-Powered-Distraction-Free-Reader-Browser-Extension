# ZenRead: AI-Powered Reader Mode & TTS Browser Extension

ZenRead transforms cluttered web articles into a pristine reading experience with AI-driven content extraction, offline fallback, and integrated Text-to-Speech (TTS), all while prioritizing user privacy with a zero-server, zero-tracking architecture.

---

## Table of Contents

*   [About ZenRead](#about-zenread)
*   [Core Features](#core-features)
*   [Architecture](#architecture)
*   [AI Agent Directives](#ai-agent-directives)
*   [Development Setup](#development-setup)
*   [Contributing](#contributing)
*   [License](#license)

---

## About ZenRead

In the age of information overload, ZenRead stands as a beacon of clarity and focus. This privacy-first browser extension is meticulously engineered to strip away distracting elements from web articles, presenting users with a clean, minimalist reader mode. Leveraging advanced AI (Google Gemini) for intelligent content extraction, it ensures the essence of the article is preserved. For seamless offline reading, it integrates Readability.js. Furthermore, an integrated Text-to-Speech engine with word highlighting enhances accessibility, reading the content aloud with synchronized highlighting. Crucially, ZenRead operates entirely client-side, meaning no servers are involved, no user data is tracked, and no personal information is ever transmitted, upholding the highest standards of user privacy.

## Core Features

*   **AI-Powered Reader Mode:** Utilizes Google Gemini to intelligently identify and extract main article content, adapting to diverse website structures.
*   **Distraction-Free Interface:** Presents articles in a clean, customizable, and minimalist layout.
*   **Offline Fallback:** Employs Readability.js for robust article parsing when AI extraction might be unavailable or less optimal.
*   **Integrated Text-to-Speech (TTS):** Reads articles aloud with synchronized word highlighting for an enhanced auditory experience.
*   **Privacy-First Architecture:** Operates exclusively in the browser, requiring no server-side processing and guaranteeing zero tracking or data collection.
*   **Multi-Browser Support:** Compatible with Chrome, Firefox, and Edge.
*   **Manifest V3 Compliant:** Built with the latest browser extension standards.

## Architecture

ZenRead employs a client-side architecture focused on modularity and performance. The core components include:

*   **Content Scripts:** Injected into web pages to interact with the DOM, extract content, and communicate with the background script.
*   **Background Script (Service Worker):** Manages extension logic, AI interactions, TTS playback, and inter-script communication.
*   **Popup UI:** Provides user controls for activation, customization, and TTS management.
*   **AI Integration Layer:** Interfaces with the Google Gemini API for advanced content summarization and extraction.
*   **Parsing Engine:** Combines AI extraction with Readability.js for comprehensive article parsing.

mermaid
graph TD
    A[Browser Page] --> B{Content Script}
    B --> C[AI Extraction (Gemini API)]
    B --> D[Readability.js]
    C --> E{Processed Content}
    D --> E
    E --> F[Background Script (Service Worker)]
    F --> G[TTS Engine]
    G --> H(Audio Output)
    F --> I[Popup UI]
    I <--> F
    J[User Interaction] --> I
    J --> F


## AI Agent Directives

<details>
<summary>Click to expand AI Agent Directives</summary>

# SYSTEM: APEX TECHNICAL AUTHORITY & ELITE ARCHITECT (DECEMBER 2025 EDITION)

## 1. IDENTITY & PRIME DIRECTIVE
**Role:** You are a Senior Principal Software Architect and Master Technical Copywriter with **40+ years of elite industry experience**. You operate with absolute precision, enforcing FAANG-level standards and the wisdom of "Managing the Unmanageable."
**Context:** Current Date is **December 2025**. You are building for the 2026 standard.
**Output Standard:** Deliver **EXECUTION-ONLY** results. No plans, no "reporting"—only executed code, updated docs, and applied fixes.
**Philosophy:** "Zero-Defect, High-Velocity, Future-Proof."

---

## 2. INPUT PROCESSING & COGNITION
*   **SPEECH-TO-TEXT INTERPRETATION PROTOCOL:**
    *   **Context:** User inputs may contain phonetic errors (homophones, typos).
    *   **Semantic Correction:** **STRICTLY FORBIDDEN** from executing literal typos. You must **INFER** technical intent based on the project context.
    *   **Logic Anchor:** Treat the `README.md` as the **Single Source of Truth (SSOT)**.
*   **MANDATORY MCP INSTRUMENTATION:**
    *   **No Guessing:** Do not hallucinate APIs.
    *   **Research First:** Use `linkup`/`brave` to search for **December 2025 Industry Standards**, **Security Threats**, and **2026 UI Trends**.
    *   **Validation:** Use `docfork` to verify *every* external API signature.
    *   **Reasoning:** Engage `clear-thought-two` to architect complex flows *before* writing code.

---

## 3. CONTEXT-AWARE APEX TECH STACKS (LATE 2025 STANDARDS)
**Directives:** Detect the project type and apply the corresponding **Apex Toolchain**. This repository, `ZenRead-AI-Reader-Mode-And-TTS-Browser-Extension`, is a JavaScript-based browser extension.

*   **PRIMARY SCENARIO: WEB / APP / EXTENSION (TypeScript / JavaScript)**
    *   **Stack:** This project leverages **JavaScript (ES2020+)** with a focus on **Manifest V3** standards. For build and tooling, it uses **Vite 7** for efficient bundling. UI elements and state management are handled with **vanilla JavaScript** or a lightweight framework if dependencies allow, prioritizing minimal bundle size. State management follows a robust, asynchronous pattern suitable for browser extensions.
    *   **Linting & Formatting:** **Biome** is mandated for its speed and comprehensive code quality features, ensuring consistency across the codebase.
    *   **Testing:** **Vitest** is the standard for unit and integration testing, providing fast feedback loops. **Playwright** is used for end-to-end testing of the extension's behavior within actual browser environments.
    *   **Architecture:** Follows a **Modular Monolith** pattern for the extension's internal structure, with clear separation of concerns between content scripts, background service workers, and UI components. **Feature-Sliced Design (FSD)** principles are encouraged for managing complexity within feature modules.
    *   **AI Integration:** Deeply integrated with **Google Gemini API** (`gemini-3-pro` by default) for intelligent article extraction. Prioritize modular design, clear API contracts, and robust error handling for all AI model interactions. Ensure all API calls are asynchronous and handled within Web Workers or Service Workers to prevent UI blocking.

*   **SECONDARY SCENARIO: SYSTEMS / PERFORMANCE (Rust / Go) - *Not applicable for this project.***
*   **TERTIARY SCENARIO: DATA / AI / SCRIPTS (Python) - *Not applicable for this project.***

---

## 4. CODE QUALITY & VERIFICATION MANDATES
*   **Linting & Formatting:** **Biome** is the sole tool. Run `biome check --apply` for automatic fixes.
*   **Unit Testing:** **Vitest** is the standard. Run `vitest` to execute all tests.
*   **End-to-End Testing:** **Playwright** is the standard. Run `npx playwright test` to execute E2E tests.
*   **Build:** Run `vite build` for production builds.

---

## 5. SECURITY PROTOCOLS
*   **Vulnerability Scanning:** Integrate `npm audit` or `yarn audit` into CI pipelines.
*   **Dependency Management:** Keep dependencies updated using `uv` (if applicable) or equivalent, with a focus on security advisories.
*   **API Key Management:** **NEVER** embed API keys directly in the codebase. Use environment variables or secure browser storage mechanisms, accessible only by the background script or service worker.
*   **Data Handling:** Adhere to strict privacy principles. No PII collected or transmitted. All AI processing is done via the Gemini API, with clear acknowledgment of Google's data handling policies if applicable to the context of usage.

---

## 6. REPOSITORY STANDARDS & BEST PRACTICES
*   **Naming Convention:** `Product-Function-Platform-Type` (e.g., `ZenRead-AI-Reader-Mode-And-TTS-Browser-Extension`).
*   **README.md:** Must be a self-contained Project Operating System. Include badges, architecture diagrams, setup, and development standards.
*   **AGENTS.md:** This document serves as the AI's operational mandate.
*   **CONTRIBUTING.md:** Clear guidelines for community contributions.
*   **LICENSE:** Use `CC BY-NC 4.0`.
*   **`.gitignore`:** Comprehensive ignore file for the specific stack.
*   **CI/CD:** Automated workflows for linting, testing, and building.
*   **ISSUE_TEMPLATE / PULL_REQUEST_TEMPLATE:** Standardized templates for issue reporting and PRs.
*   **SECURITY.md:** Outline security policies and reporting mechanisms.

---

## 7. OPERATIONAL COMMANDS (DECEMBER 2025 EDITION)
*   **Install Dependencies:** `npm install` or `yarn install`
*   **Lint & Format:** `npx @biomejs/biome check --apply`
*   **Run Tests:** `npx vitest`
*   **E2E Tests:** `npx playwright test`
*   **Development Server:** `npm run dev` or `yarn dev`
*   **Build for Production:** `npm run build` or `yarn build`
*   **AI Interaction:** Refer to `./src/services/geminiService.js` for example usage patterns. Ensure API keys are managed securely via `.env` files and are **NOT** committed.

</details>

---

## Development Setup

Follow these steps to set up the development environment:

1.  **Clone the repository:**
    bash
    git clone https://github.com/chirag127/ZenRead-AI-Reader-Mode-And-TTS-Browser-Extension
    cd ZenRead-AI-Reader-Mode-And-TTS-Browser-Extension
    

2.  **Install Node.js (v18.x or higher recommended):**
    If you don't have Node.js installed, download it from [nodejs.org](https://nodejs.org/).

3.  **Install dependencies:**
    bash
    npm install
    # or
    yarn install
    

4.  **Configure Environment Variables:**
    Create a `.env` file in the root directory and add your Google Gemini API key:
    
    VITE_GEMINI_API_KEY=YOUR_GEMINI_API_KEY
    
    **IMPORTANT:** Add `.env` to your `.gitignore` file to prevent accidental commits of your API key.

5.  **Run in development mode:**
    This will start a development server and automatically reload the extension upon changes.
    bash
    npm run dev
    # or
    yarn dev
    

6.  **Load the extension in your browser:**
    *   **Chrome/Edge:** Navigate to `chrome://extensions/` (or `edge://extensions/`), enable **Developer mode**, click **Load unpacked**, and select the `dist` folder (or the folder specified by Vite's build output).
    *   **Firefox:** Navigate to `about:debugging#/runtime/this-firefox`, click **Load Temporary Add-on**, and select the `manifest.json` file.

## Scripts

| Script          | Description                                                               |
| --------------- | ------------------------------------------------------------------------- |
| `dev`           | Run the Vite development server for live reloading.                       |
| `build`         | Build the extension for production deployment.                            |
| `lint`          | Run Biome to check and format code.                                       |
| `test`          | Execute all unit and integration tests with Vitest.                       |
| `test:e2e`      | Execute end-to-end tests with Playwright.                                 |

## Contributing

Contributions are welcome! Please refer to the [CONTRIBUTING.md](https://github.com/chirag127/ZenRead-AI-Reader-Mode-And-TTS-Browser-Extension/blob/main/.github/CONTRIBUTING.md) file for detailed guidelines on how to submit bug reports, feature requests, and pull requests.

We adhere to the principles of **SOLID**, **DRY**, and **YAGNI** to ensure maintainable and scalable code.

## License

This project is licensed under the **Creative Commons Attribution-NonCommercial 4.0 International (CC BY-NC 4.0)** license. See the [LICENSE](https://github.com/chirag127/ZenRead-AI-Reader-Mode-And-TTS-Browser-Extension/blob/main/LICENSE) file for more details.

---

<p align="center">
  <a href="#" target="_blank">
    <img src="https://img.shields.io/github/stars/chirag127/ZenRead-AI-Reader-Mode-And-TTS-Browser-Extension?style=flat-square" alt="GitHub Stars">
  </a>
  <a href="#" target="_blank">
    <img src="https://img.shields.io/github/forks/chirag127/ZenRead-AI-Reader-Mode-And-TTS-Browser-Extension?style=flat-square" alt="GitHub Forks">
  </a>
  <a href="#" target="_blank">
    <img src="https://img.shields.io/github/license/chirag127/ZenRead-AI-Reader-Mode-And-TTS-Browser-Extension?style=flat-square" alt="License">
  </a>
  <a href="#" target="_blank">
    <img src="https://img.shields.io/github/actions/workflow/status/chirag127/ZenRead-AI-Reader-Mode-And-TTS-Browser-Extension/ci.yml?style=flat-square" alt="Build Status">
  </a>
  <a href="#" target="_blank">
    <img src="https://img.shields.io/codecov/c/github/chirag127/ZenRead-AI-Reader-Mode-And-TTS-Browser-Extension?style=flat-square" alt="Code Coverage">
  </a>
  <a href="#" target="_blank">
    <img src="https://img.shields.io/badge/JavaScript-ES2020+-blue?style=flat-square" alt="Tech Stack: JavaScript">
  </a>
  <a href="#" target="_blank">
    <img src="https://img.shields.io/badge/Vite-7.x-purple?style=flat-square" alt="Tech Stack: Vite">
  </a>
  <a href="#" target="_blank">
    <img src="https://img.shields.io/badge/Biome-latest-brightgreen?style=flat-square" alt="Lint/Format: Biome">
  </a>
  <a href="#" target="_blank">
    <img src="https://img.shields.io/badge/License-CC BY-NC 4.0-orange?style=flat-square" alt="License: CC BY-NC 4.0">
  </a>
</p>

