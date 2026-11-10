# LocalGravity (`v0.9.5-beta`)

[![Release](https://img.shields.io/badge/Download-Release%20v0.9.5--beta-blue.svg?style=for-the-badge&logo=github)](https://github.com/toesmax/LocalGravity/releases/latest)
[![Windows](https://img.shields.io/badge/Windows-Setup%20%26%20Portable-0078D6.svg?style=for-the-badge&logo=windows)](https://github.com/toesmax/LocalGravity/releases/latest)
[![macOS](https://img.shields.io/badge/macOS-Apple%20Silicon%20%26%20Intel-000000.svg?style=for-the-badge&logo=apple)](https://github.com/toesmax/LocalGravity/releases/latest)
[![License: Proprietary EULA](https://img.shields.io/badge/License-Proprietary%20EULA-red.svg?style=for-the-badge)](./LICENSE)

> **Autonomous Local & Hybrid AI Engineering Workstation**  
> A privacy-first desktop agentic IDE built for local LLMs (Ollama, LM Studio, Llama.cpp / GGUF) and frontier Cloud AI (Gemini, OpenAI, Anthropic) — featuring true physical workspace isolation, a Strict Local-Only Firewall, 13 chainable slash commands, and 29 specialized engineering studios.

---

## 📥 Downloads & Installation

Get the latest pre-compiled desktop binary for your system from the [**Releases Page**](https://github.com/toesmax/LocalGravity/releases/latest):

| Platform | Package Type | Description |
| :--- | :--- | :--- |
| **Windows** | `LocalGravity-Setup-0.9.5-beta-x64.exe` | **Interactive Setup Wizard (NSIS)** — Select install directory, creates Desktop & Start Menu shortcuts. |
| **Windows** | `LocalGravity-Portable-0.9.5-beta-x64.exe` | **Standalone Portable Executable** — Zero installation required. Double-click to launch anywhere. |
| **macOS** | `LocalGravity-macOS.zip` | **macOS Portable Kit** — Native support for Apple Silicon (M1–M4 Metal acceleration) and Intel. |

---

## 🌟 Key Features

### 1. 100% Local & Hybrid Model Orchestration (Zero-Leakage Privacy)
- **Local Model Connectivity**: Seamlessly connect to locally hosted models via **Ollama** (`127.0.0.1:11434`), **LM Studio** (`127.0.0.1:1234`), **vLLM**, or raw **Llama.cpp (GGUF)** binaries.
- **Frontier Cloud Integration**: Switch on-demand to **Google Gemini** (official `@google/genai` SDK), **OpenAI**, or **Anthropic Claude**.
- **Strict Local-Only Firewall (Optional)**: When engaged for local models, LocalGravity blocks all outbound internet traffic and unexpected remote fallbacks, guaranteeing that your source code, prompts, and workspace files never leave your machine.
- **Multi-Format Parser & Auto-Materialization**: Compact local models (`7B`–`14B`) that lack native JSON function-calling are automatically parsed and translated into deterministic filesystem writes, edits, and terminal executions.

### 2. Bilingual Support with English-First Defaults
- **English as Default**: The user interface, system prompts, default studio templates, and agent interactions default to English for global workflows.
- **Instant Language Switcher**: Toggle between 🇬🇧 **English (Default)** and 🇮🇹 **Italiano** at any moment via the top-bar `🌐 EN/IT` button or during the First-Run Setup Wizard.

### 3. Physical Workspace Isolation & Ephemeral Workspaces
- **Real Filesystem Mapping**: Every workspace is mapped to an isolated directory on disk (`/workspaces/<Project-Name>` or any custom folder).
- **Procedural Ephemeral Workspaces with Auto-Cleanup**: On launch, LocalGravity provisions a clean procedural workspace (e.g., `Quantum-Prism`, `Logic-Core`). If you switch to an existing project before sending a prompt, the ephemeral folder is automatically purged to keep your disk clean.
- **Context Continuity**: The agent inspects active workspace files prior to applying edits, eliminating context amnesia across conversation turns.

### 4. 4 Fine-Grained Autonomy Levels
| Autonomy Mode | Description |
| :--- | :--- |
| **`Chat-Only`** | Advisory mode. Explains code and designs architecture without touching files or running commands. |
| **`Supervised`** | Interactive approval dialog displayed before every file write, diff, or shell command. |
| **`Default`** | Workspace file modifications are auto-approved; destructive or system-wide commands trigger guardrails. |
| **`Turbo`** | Autonomous end-to-end execution loop with automated compilation, testing, and self-repair. |

### 5. 13 Chainable Slash Commands
Commands can be concatenated inside a single prompt (e.g. `/plan /goal Build a TypeScript REST API with full test coverage`):

| Command | Function |
| :--- | :--- |
| `/plan` | Generates a structured `PROJECT_PLAN.md` and begins step-by-step implementation |
| `/goal` | Autonomous loop: executes and iterates until all verification criteria pass |
| `/grill-me` | Conducts a technical requirements interview, synthesizes `SPEC.md`, and implements the project |
| `/boost` | Multi-agent parallel orchestration (*Investigator* + *Coder* + *Verifier*) |
| `/teamwork-preview` | Coordinated Swarm worktree execution supervised by an Auditor agent |
| `/learn` | Extracts project architecture patterns and saves them to persistent project memory |
| `/compact` | Compresses conversation context while preserving critical architecture decisions and touched files |
| `/btw` | Fast contextual side-question without interrupting or resetting the active task |
| `/model` | Hot-swaps the active AI model mid-session and continues execution seamlessly |
| `/agents` | Inspects, directs, or terminates running subagents |
| `/mcp` | Discovers and executes tools from Model Context Protocol (MCP) servers |
| `/branch` | Branches the current conversation into an isolated parallel thread |
| `/workspace` | Switches or provisions a new isolated workspace on disk |

### 6. 29 Integrated Engineering Studios
All 29 Studios operate directly on the real workspace files and can dispatch background tasks to the agent:

- **Development & Code Quality**:
  - `Auto-Heal TDD`: Autonomous test-driven development loop (Red ➔ Green ➔ Refactor).
  - `Code Health Heatmap`: Visual technical debt & complexity analysis.
  - `Codemod AST`: Structural abstract syntax tree transformations.
  - `Polyglot Playground`: Instant code execution across multiple languages.
  - `DocuStudio`: Automated API and architecture documentation generator.
  - `BundleCraft`: Frontend asset inspection, bundle size analysis, and optimization.
  - `PromptCraft`: Systematic prompt engineering, evaluation, and tuning.
  - `SchemaCraft`: Visual OpenAPI / JSON Schema designer and validator.

- **Architecture, Security & Planning**:
  - `Graph Radar`: Interactive dependency graphs and module topology.
  - `Council Sentry`: Adversarial multi-agent code and security reviews.
  - `EnvVault & Secret Scanner`: High-entropy credential detection and safe environment injection.
  - `Consensus Matrix`: Multi-model decision comparison matrix.
  - `FlowForge`: Workflow diagramming and visual state machine designer.
  - `Automations`: Cron and scheduled background agent jobs.

- **Infrastructure, Network, Data & Hardware**:
  - `GitForge`: Interactive visual Git staging, branching, and commit management.
  - `ContainerCraft`: Dockerfile generation, linting, and container lifecycle controls.
  - `PipelineCraft`: CI/CD workflow generator (GitHub Actions, GitLab CI).
  - `MockLab Server`: Instant mock REST and GraphQL server engine.
  - `NetCraft`: Interactive HTTP/cURL API client with request replay.
  - `StreamCraft`: Real-time WebSocket and Server-Sent Events (SSE) debugger.
  - `QueryCraft`: SQL query builder, execution analyzer, and migration manager.
  - `DataForge`: Synthetic dataset generation and schema mocking.
  - `PerfBench`: CPU, memory, and latency benchmarking.
  - `SysPulse`: Real-time GPU VRAM, CPU utilization, and thermal monitoring.
  - `Cluster Multi-PC`: Distributed model inference across local network machines.
  - `MCP Marketplace`: One-click Model Context Protocol server catalog.
  - `Skills Manager`: Hot-pluggable agent skill management.
  - `NotifyCraft`: Desktop and webhooks notification dispatch.
  - `Voice Studio`: Speech-to-Text and voice control studio.

---

## 🔒 Credential Security (`safeStorage` & AES-256-GCM)

API keys configured in the **Setup Wizard** or **Settings** are securely encrypted using the operating system's native keychain:
- **Windows**: DPAPI via Electron `safeStorage`
- **macOS**: Apple Keychain
- **Linux**: Secret Service API / libsecret

Fallback storage utilizes an authenticated `AES-256-GCM` encrypted vault stored at `~/.localgravity/credentials.vault.json`. **No credentials or API keys are ever stored unencrypted.**

---

## ⚠️ Disclaimer & Responsible AI Use

LocalGravity is a desktop development workstation and runtime execution environment. It does not bundle, host, or distribute proprietary AI weights or uncensored foundation models. 

Users are solely responsible for:
- Ensuring that any third-party, remote, or local AI models connected to LocalGravity comply with all applicable local, national, and international laws, regulations, and licensing terms.
- The legality, ethics, security, and consequences of prompts, shell commands, code modifications, or content generated using this workstation.
- Reviewing and validating any automated changes before execution or deployment.

The authors, maintainers, and contributors disclaim any liability for improper, unauthorized, malicious, or illegal use of the software.

---

## 📄 License & Terms of Use

LocalGravity is proprietary software distributed under the terms of the **LocalGravity End User License Agreement (EULA)**. It is free for personal, educational, research, and internal commercial development use. 

Decompilation, reverse engineering, unauthorized redistribution, extraction of underlying source code, and commercial resale of the software or its binaries are strictly prohibited without prior written permission from the authors. See [`LICENSE`](./LICENSE) for the full legal agreement.

---

**Created by Andrea Straniero and Matteo Straniero with special thanks to Tommaso Costanza for his UX | UI contributions.**
