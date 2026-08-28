# PROTOCOL.md: Skill-Driven Development Ecosystem

**Languages:** **English** · [Русский](PROTOCOL_ru.md) · [العربية](PROTOCOL_ar.md) · [中文](PROTOCOL_zh.md) · [Deutsch](PROTOCOL_de.md) · [Español](PROTOCOL_es.md) · [Français](PROTOCOL_fr.md) · [日本語](PROTOCOL_ja.md) · [한국어](PROTOCOL_ko.md) · [Português](PROTOCOL_pt.md)

## 1. Concept and Philosophy

This document describes the development methodology within the portfolio, adapted for a hybrid agent ecosystem. The protocol covers the entire product lifecycle—from the initial architectural draft to the final generation of presentation artifacts.

Core principle: **Architectural decisions must be explicit, reproducible, and defensible.** We have transitioned from simply writing code to **Skill-Driven Development**, where routine operations, design, testing, and analytics are delegated to specialized skills of specific agents.

---

## 2. Roles and Skill Distribution

Three main entities participate in the process. Their roles are strictly separated and do not overlap.

### 2.1. Developer (Human)
The product owner. Has the final say on every architectural decision point, approves the scope, sets the development direction, and accepts the agents' deliverables.

### 2.2. OpenCode (Autonomous Implementer)
The executing agent, operating in the terminal with a context window of up to 1M tokens. Responsible for writing code, building interfaces, and generating documents and media artifacts. 
Possesses the following arsenal of skills:
*   **Engineering and Code:** `code-review-skill`, `webapp-testing`, `mcp-builder`, `skill-creator`, `claude-api`.
*   **Design and Frontend:** `frontend-design`, `web-artifacts-builder`, `theme-factory`, `canvas-design`, `algorithmic-art`, `brand-guidelines`.
*   **Documentation and Office:** `build-project-docs`, `doc-coauthoring`, `docx`, `pdf`, `pptx`, `xlsx`.
*   **Communications and Training:** `academy-guide`, `internal-comms`, `slack-gif-creator`, `discernment-nudge`.

### 2.3. Claude Desktop (Architect and Analyst)
Acts as the Data Center and architectural reviewer. Does not write production code directly, but verifies logic, analyzes database data, and formulates tasks for OpenCode.
Arsenal of skills:
*   **Context Management:** `morning`, `Import-memory`, `skill-creator`, `doc-coauthoring`.
*   **Analytics and Validation:** `analyze`, `data-context-extractor`, `explore-data`, `validate-data`, `statistical-analysis`.
*   **DB and Data Visualization:** `sql-queries`, `write-query`, `build-dashboard`, `create-viz`, `data-visualization`.

### 2.4. Antigravity (Unified Agentic Environment)
A fully autonomous environment that integrates the complete set of 33 skills.
*   **Key Rule:** All project documentation must henceforth be created and maintained exclusively through Antigravity, leveraging Gemini and Claude models (as the premier documentation tools with unrestricted access to skills).

---

## 3. Protocol Stages (Project Lifecycle)

### Stage 1: Initialization and ARCHITECTURE.md
The architecture is formulated before a single line of code is written.
1.  **Claude Desktop** activates the `morning` and `Import-memory` skills to load context and previous work. Then applies `analyze` to decompose requirements.
2.  **OpenCode** uses `build-project-docs` to create a draft of `ARCHITECTURE.md`.
3.  The document solidifies: data structures, storage formats, the tech stack, and module breakdown.

### Stage 2: Grill-me (Architecture Stress-Test)
Architecture is not taken on faith. It must be attacked.
1.  **Claude Desktop** applies `data-context-extractor` to identify "blind spots" in the data and `doc-coauthoring` to generate uncomfortable questions.
2.  **OpenCode** may use `discernment-nudge` for critical self-assessment of the proposed technical solutions.
3.  Every contentious decision point is closed with a triad: **chosen solution -> reason for rejecting the alternative -> exclusions from the scope**.

### Stage 3: Deliberate Deviations
A section in `ARCHITECTURE.md` where we log all features and capabilities that we **consciously choose not to build**. The boundary of a project's capabilities is a full-fledged part of its architecture. If a decision changes during development, the old decision is moved here along with the reason.

### Stage 4: Module-by-Module Implementation
Development proceeds bottom-up along the dependency graph.
1.  **OpenCode** implements the project core. For integrations and protocols, `mcp-builder` and `claude-api` are utilized.
2.  When working on the visual side, **OpenCode** activates the chain: `brand-guidelines` -> `theme-factory` -> `frontend-design` -> `web-artifacts-builder`.
3.  For procedural graphics generation or complex canvases, `algorithmic-art` and `canvas-design` are applied.

### Stage 5: Code-review & Testing
Verification is always separated from writing code.
1.  **OpenCode** performs a separate pass using `code-review-skill`, identifying bugs and compromises.
2.  UI and integration testing is conducted via the `webapp-testing` skill. Test output (stdout/stderr) is saved without modifications.
3.  **Claude Desktop** steps in to verify data handling: it uses `sql-queries` and `write-query` to check database integrity, alongside `validate-data` and `statistical-analysis` to verify business logic.

### Stage 6: Artifact and Analytics Generation
The project must be presented to the user or stakeholders.
1.  **Claude Desktop**, using `build-dashboard`, `create-viz`, and `data-visualization`, forms reports based on application results or metrics.
2.  **OpenCode** packages this data into ready-made business artifacts:
    *   Reports and specs: `pdf`, `docx`, `xlsx` skills.
    *   Architecture presentations: `pptx` skill.
    *   Training and internal materials: `academy-guide`, `internal-comms`.
    *   Dynamic content for announcements: `slack-gif-creator`.

### Stage 7: Final Checklist
Before release, the following are verified:
*   Synchronization of the final code with `ARCHITECTURE.md`.
*   Presence of actual test logs.
*   Absence of temporary files, caches, and secret keys.

---

## 4. Model Selection Policy

OpenCode runs on free models, the choice of which is dictated by the task:

| Model | Role | Purpose | Privacy Status |
| :--- | :--- | :--- | :--- |
| **Muse Spark 1.2 Free** | Autonomous Agent (Core) | Execution of the main skill matrix, 1M token context, multi-step logic in the terminal. | Permanent free-tier |
| **Nemotron 3 Ultra Free** | Deep Analyst | Heavy mathematics, complex algorithms, large-scale system refactoring. | **NVIDIA trial** — data is logged to improve the product. |
| **Nemotron 3.5 Lightning Free** | Background Executor | Fast validation, utilitarian function calls, mass pipeline processing. | **NVIDIA trial** — same as Ultra. |
| **MiMo V2.5 Free** | UI/UX Assistant | Screenshot debugging, on-the-fly `frontend-design`. | Temporary free-period. |

For **Antigravity**, **Gemini 3.5 Flash (Medium)** is used as the primary engine to ensure minimal consumption of limits/quotas and allow continuous work on tasks and documentation.

**Security Restriction:** It is **strictly forbidden** to pass private keys, tokens, real databases, and private repositories into trial endpoints (Nemotron, MiMo). Only a local or trusted environment is used for sensitive data.

---

## 5. Core Ecosystem Principles

1. **An explicit decision is better than a convenient default.** If an agent hits a crossroads, it does not guess; it formulates options and waits for approval (or logs a compromise).
2. **Skills are used for their intended purpose.** There is no need to generate Markdown tables if an Excel report is required (use `xlsx`). There is no need to describe a dashboard in text (use `build-dashboard` + `create-viz`).
3. **A bug caught in review means a working system.** A finding during the review stage via `code-review-skill` is proof that the two-stage filter works.
4. **Project boundaries are inviolable.** A half-finished "do-it-all" tool is worse than a highly specialized tool with a clearly documented Deliberate Deviations section.