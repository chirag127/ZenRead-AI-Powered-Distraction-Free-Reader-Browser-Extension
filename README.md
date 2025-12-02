# ZenRead: AI-Powered Distraction-Free Reader Browser Extension

> The ultimate tool for focused, intelligent content consumption on the web. Leverage Gemini AI to transform cluttered pages into clean, summarized, and acoustically accessible content streams.

<p align="center">
  <a href="https://github.com/chirag127/ZenRead-AI-Powered-Distraction-Free-Reader-Browser-Extension/actions/workflows/ci.yml" target="_blank">
    <img alt="Build Status" src="https://img.shields.io/github/actions/workflow/status/chirag127/ZenRead-AI-Powered-Distraction-Free-Reader-Browser-Extension/ci.yml?branch=main&style=flat-square&label=CI%20Build" />
  </a>
  <a href="https://github.com/chirag127/ZenRead-AI-Powered-Distraction-Free-Reader-Browser-Extension/blob/main/LICENSE" target="_blank">
    <img alt="License" src="https://img.shields.io/badge/License-CC%20BY--NC%204.0-blue.svg?style=flat-square" />
  </a>
  <a href="https://github.com/chirag127/ZenRead-AI-Powered-Distraction-Free-Reader-Browser-Extension" target="_blank">
    <img alt="Stars" src="https://img.shields.io/github/stars/chirag127/ZenRead-AI-Powered-Distraction-Free-Reader-Browser-Extension?style=flat-square&label=Stars&color=yellow" />
  </a>
  <img alt="Tech Stack" src="https://img.shields.io/badge/Stack-WXT%20%7C%20JS%20%7C%20AI-209E61.svg?style=flat-square" />
  <img alt="Linting" src="https://img.shields.io/badge/Linter-Biome-60A5FA.svg?style=flat-square" />
  <a href="https://www.codecov.io/gh/chirag127/ZenRead-AI-Powered-Distraction-Free-Reader-Browser-Extension" target="_blank">
    <img alt="Coverage" src="https://img.shields.io/codecov/c/github/chirag127/ZenRead-AI-Powered-Distraction-Free-Reader-Browser-Extension?style=flat-square&token=YOUR_TOKEN_HERE" />
  </a>
</p>

***

<p align="center">
  <a href="https://github.com/chirag127/ZenRead-AI-Powered-Distraction-Free-Reader-Browser-Extension">
    <img src="https://img.shields.io/badge/⭐%20Star%20this%20Repo-Support%20Open%20Source-ff69b4.svg?style=for-the-badge&logo=github" alt="Star this Repository" />
  </a>
</p>

ZenRead transforms cluttered web pages into clean, highly readable, and acoustically accessible content streams. Leveraging the power of Google Gemini AI, it not only removes distractions but also intelligently summarizes, translates, and processes text, ensuring absolute focus and maximum comprehension.

## 🚀 Key Features

*   **One-Click Zen Mode:** Instantaneously strips away advertisements, pop-ups, and extraneous UI elements.
*   **AI Contextual Summary:** Uses Gemini 1.5 Pro to generate a concise summary of the extracted article content.
*   **Seamless Text-to-Speech (TTS):** High-quality, native voice synthesis for auditory learning.
*   **Cross-Browser Compatibility:** Built using WXT for rapid deployment across Chrome, Firefox, and Edge.
*   **Privacy-Focused:** Content processing happens locally where possible, with explicit AI consent.

## 🏛️ Architecture Overview

ZenRead utilizes the **Feature-Sliced Design (FSD)** methodology, which is ideal for isolating extension components (e.g., popup, content script, background service) into highly cohesive, domain-specific layers.

mermaid
graph TD
    A[User Action: Click ZenRead Icon] --> B(Content Script: DOM Extraction);
    B --> C{Background Service Worker};
    C --> D(Module: Text Cleaning & Serialization);
    C --> E(Module: Gemini AI API Integration);
    E --> F(AI Summary & Processing);
    F --> G(Module: State Management (e.g., Zustand/Chrome Storage));
    G --> H(Popup/Sidebar UI Update);
    C --> I(Module: TTS Synthesis & Playback);


## 📖 Table of Contents

1.  [🚀 Key Features](#-key-features)
2.  [🏛️ Architecture Overview](#-architecture-overview)
3.  [🤖 AI Agent Directives (System SSOT)](#-ai-agent-directives-system-ssot)
4.  [💻 Development Setup](#-development-setup)
5.  [📜 Scripts and Commands](#-scripts-and-commands)
6.  [🌐 Principles & Standards](#-principles--standards)
7.  [🤝 Contributing](#-contributing)
8.  [© License](#-license)

## 🤖 AI Agent Directives (System SSOT)

<details>
<summary>⚡ APEX LATE 2025 ENGINEERING STANDARDS & DIRECTIVES</summary>

### Identity & Context
This repository, `ZenRead-AI-Powered-Distraction-Free-Reader-Browser-Extension`, is a critical, privacy-focused browser extension utilizing JavaScript, the WXT framework, and Google Gemini APIs. All code generation and refactoring MUST adhere to maximum performance and minimal memory footprint, essential for browser extensions.

### Apex Toolchain (2026 Standard)
| Tool | Purpose | Directive |
| :--- | :--- | :--- |
| **WXT Framework** | Extension Scaffolding/Vite Integration | Utilize Manifest V3, optimize background service worker execution models. |
| **Biome** | Linter/Formatter/JS Checker | Enforcement of absolute code style consistency (`biome check --apply`). |
| **Vitest** | Unit & Integration Testing | Target 100% coverage on all content extraction and AI prompt modules. |
| **TypeScript (Migration Path)** | Static Type Safety | All new modules MUST be written in strict TypeScript. Refactor legacy JS files incrementally. |
| **Node.js (LTS)** | Runtime Environment | Use Node v20+ for development and CI/CD pipelines. |

### Architectural Enforcement
1.  **Feature-Sliced Design (FSD):** Strictly enforce FSD principles. Components must be atomic, reusable, and separated by scope (app/pages/widgets/features/entities/shared). No imports between features in a horizontal manner (Feature A importing from Feature B).
2.  **SOLID & DRY:** Maximize modularity. The AI interaction layer (`src/features/ai-processing`) must be decoupled from the UI/Content Script layers via message passing.
3.  **Content Script Isolation:** Content scripts must be lean, focusing only on DOM manipulation and extraction, delegating heavy computation (AI/TTS processing) to the Background Service Worker via Chrome Message Passing API.

### Verification and Delivery
| Command | Description | Purpose |
| :--- | :--- | :--- |
| `npm run build` | Generates distributable package. | MUST complete with zero warnings. |
| `npm run lint:check` | Runs Biome checks. | MUST pass clean before any commit. |
| `npm run test` | Executes Vitest unit tests. | Maintain minimum 95% line coverage. |
| `npm run check:types` | Runs TSC compiler checks. | Ensures TypeScript integrity during JS refactoring. |

</details>

## 💻 Development Setup

This project uses `npm` and the WXT framework for development.

1.  **Prerequisites:** Ensure Node.js (v20+) is installed.
2.  **Clone the Repository:**
    bash
    git clone https://github.com/chirag127/ZenRead-AI-Powered-Distraction-Free-Reader-Browser-Extension.git
    cd ZenRead-AI-Powered-Distraction-Free-Reader-Browser-Extension
    
3.  **Install Dependencies:**
    bash
    npm install
    
4.  **Environment Variables:** Create a `.env` file in the root directory for your AI key.
    
    # Required for AI Summarization Feature
    GEMINI_API_KEY="YOUR_GEMINI_KEY"
    
5.  **Start Development Mode:**
    bash
    npm run dev
    # Loads the extension into the browser for hot-reloading.
    

## 📜 Scripts and Commands

| Script | Command | Description |
| :--- | :--- | :--- |
| `dev` | `wxt:dev` | Starts the development server for hot module reloading. |
| `build` | `wxt build` | Compiles the production-ready extension bundle. |
| `lint` | `biome lint .` | Executes Biome linting checks. |
| `format` | `biome format .` | Auto-formats code using Biome standards. |
| `test` | `vitest` | Runs all unit and integration tests (coverage recommended). |
| `clean` | `rm -rf .output && rm -rf node_modules` | Clears all built artifacts and modules. |

## 🌐 Principles & Standards

We strictly adhere to core architectural philosophies to ensure maintainability and scalability.

*   **SOLID:** Single Responsibility Principle (especially critical for content scripts and background workers).
*   **DRY (Don't Repeat Yourself):** All shared utilities (e.g., content cleaning algorithms) must reside in the FSD `shared` layer.
*   **YAGNI (You Aren't Gonna Need It):** Features are implemented only when absolutely necessary, focusing on a minimal, high-utility product.
*   **Performance First:** All DOM manipulations and data processing must be asynchronous and non-blocking.

## 🤝 Contributing
ZenRead is an open-source project managed under the Apex Standard 11 compliance mandate. Please review the following documents before submitting contributions:

*   [CONTRIBUTING.md](.github/CONTRIBUTING.md) - Guidelines for code submission and architectural expectations.
*   [CODE_OF_CONDUCT.md](CODE_OF_CONDUCT.md) - Our standards for respectful engagement.
*   [SECURITY.md](.github/SECURITY.md) - Instructions for reporting vulnerabilities securely.

## © License
This project is licensed under the **Creative Commons Attribution-NonCommercial 4.0 International Public License (CC BY-NC 4.0)**.