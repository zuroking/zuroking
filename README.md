<div align="center">

<img width="100%" src="https://capsule-render.vercel.app/api?type=waving&color=0:0F172A,50:1D4ED8,100:7C3AED&height=210&section=header&text=Aldiyar%20%28Zuro%29&fontSize=58&fontColor=FFFFFF&fontAlignY=35&desc=AI%2FML%20Engineer%20in%20progress%20%C2%B7%20Building%20from%20first%20principles&descAlignY=58&descSize=18&animation=fadeIn" />

<h1>👋 Hi, I'm Zuro</h1>

<p><strong>Developer from Astana, Kazakhstan — 15 years old</strong><br>
I build ML systems, developer tools, and computer-science projects from scratch — not from tutorials.</p>

<a href="https://github.com/zuroking">
  <img src="https://readme-typing-svg.demolab.com?font=Fira+Code&size=19&pause=1200&color=60A5FA&center=true&vCenter=true&width=760&lines=Understanding+the+mechanics%2C+not+just+calling+an+API;Transformers+%C2%B7+autodiff+%C2%B7+HNSW+%C2%B7+systems+programming;Learning+with+AI%2C+building+with+intent;One+from-scratch+project+at+a+time" alt="Profile summary" />
</a>

[![GitHub](https://img.shields.io/badge/GitHub-@zuroking-181717?style=for-the-badge&logo=github)](https://github.com/zuroking)
[![Telegram](https://img.shields.io/badge/Telegram-@Zuroking-26A5E4?style=for-the-badge&logo=telegram&logoColor=white)](https://t.me/Zuroking)
[![Email](https://img.shields.io/badge/Email-Contact-D14836?style=for-the-badge&logo=gmail&logoColor=white)](mailto:zuroking69@gmail.com)

<br>

![Open to junior roles](https://img.shields.io/badge/Junior_AI%2FML_Roles-Open-22C55E?style=for-the-badge&labelColor=14532D)
![Remote, hybrid, or on-site](https://img.shields.io/badge/Remote%2FHybrid%2FOn--site-Open-3B82F6?style=for-the-badge&labelColor=172554)

</div>

---

<div align="center">

### 🧭 Navigation

[About](#-about-me) · [Toolbox](#️-toolbox) · [Projects](#-featured-projects) · [Roadmap](#️-roadmap) · [Principles](#-engineering-principles)

</div>

---

## 🧠 About me

```python
zuro = {
    "role": "Aspiring AI Engineer",
    "location": "Astana, Kazakhstan",
    "mission": "Understand systems deeply by building them from scratch",
    "focus": [
        "Transformer internals and local LLM inference",
        "Reverse-mode autodiff and ML foundations",
        "Vector search with HNSW",
        "Systems programming, networking, and security",
    ],
    "currently_exploring": ["Ollama", "GGUF", "quantization", "PagedAttention", "KV cache"],
}
```

I build systems and ML tools **from first principles** — no shortcuts through high-level frameworks when the goal is to understand the internals. My projects skip the usual "easy" libraries (Hugging Face `Trainer`, FAISS, Gymnasium, autograd), so I own and understand the underlying mechanics: what happens inside a transformer forward pass, how gradients flow backward through a computation graph, and why an HNSW index finds approximate neighbours fast.

I use AI as a learning and building partner throughout the process — never as a substitute for understanding. Claude Code and OpenCode are part of my workflow; I use [Claude.ai](https://claude.ai) for ideas and architecture decisions, and ChatGPT to unpack code patterns I am still learning.

- 🌱 Exploring local LLM deployment (Ollama, GGUF, quantization), inference internals (PagedAttention, KV cache), and analytic number theory
- 💬 Ask me about transformer internals, reverse-mode autodiff, vector search (HNSW), and async Python architecture
- 🎯 Working toward a Junior AI/ML Engineer role — remote, hybrid, or on-site

## 🛠️ Toolbox

<div align="center">

<img src="https://img.shields.io/badge/Claude-D97757?style=for-the-badge&logo=anthropic&logoColor=white" />
<img src="https://img.shields.io/badge/OpenCode-000000?style=for-the-badge&logo=opencode&logoColor=white" />
<img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white" />
<img src="https://img.shields.io/badge/ChatGPT-74AA9C?style=for-the-badge&logo=openai&logoColor=white" />
<img src="https://img.shields.io/badge/PyTorch-EE4C2C?style=for-the-badge&logo=pytorch&logoColor=white" />
<img src="https://img.shields.io/badge/NumPy-013243?style=for-the-badge&logo=numpy&logoColor=white" />
<img src="https://img.shields.io/badge/Pydantic-E92063?style=for-the-badge&logo=pydantic&logoColor=white" />
<img src="https://img.shields.io/badge/Typer%20%2F%20Rich-000000?style=for-the-badge&logo=windowsterminal&logoColor=white" />

</div>

## 🚀 Featured projects

Completed projects. Each one starts with an architecture specification, goes through module-level review, and ships with real test results only — never fabricated output.

| Project | What I built | Engineering focus |
|---|---|---|
| [**basicthon**](https://github.com/zuroking/basicthon) | **My largest project:** a bilingual learning repository of 20 isolated Python projects, progressing from a CLI calculator to a CLI + SQLite + REST API capstone. 655 passing tests, with explicit notes marking implementations as educational-only | Structuring a large learning codebase with tests and clear scope boundaries |
| [**kronos-synapse-dialog-core**](https://github.com/zuroking/ZURO_AI) | GPT-style decoder-only language model (~15.3M parameters), CPU-only, written in pure PyTorch — built from scratch to understand transformer internals | Transformer internals: attention, positional encoding, and the training loop |
| [**vector-db-from-scratch**](https://github.com/zuroking/vector-db-from-scratch) | Custom vector database with an HNSW index in pure NumPy — no FAISS, no hnswlib | Approximate nearest-neighbour search and graph-based indexing |
| [**autograd-engine**](https://github.com/zuroking/autograd-engine) | Reverse-mode automatic differentiation engine in pure NumPy — no PyTorch or TensorFlow | Backpropagation and computational graphs — the core of every ML framework |
| [**secure-secrets-vault**](https://github.com/zuroking/secure-secrets-vault) | Encrypted local secrets CLI with master-password protection and key derivation | Applied security: encryption, KDFs, and secret-handling hygiene |
| [**sql-engine-toy**](https://github.com/zuroking/sql-engine-toy) | SQL parser, B-tree index, and simple query planner *(archived by protocol after completion)* | Database internals: parsing, storage structures, query planning |
| [**os-scheduler-sim**](https://github.com/zuroking/os-scheduler-sim) | Scheduler simulator covering Round Robin, priority scheduling, and MLFQ with Gantt-chart visualization | Operating-system concepts: scheduling algorithms and their trade-offs |
| [**http-server-from-scratch**](https://github.com/zuroking/http-server-from-scratch) | HTTP server on raw sockets: request parsing, routing, keep-alive, and basic TLS | Networking fundamentals at the protocol level |
| [**compression-codec**](https://github.com/zuroking/compression-codec) | Huffman + LZ77 codec benchmarked against gzip and zstd | Algorithms and data structures under measurable performance comparison |
| [**geometry_dash_RL_agent**](https://github.com/zuroking/GD_RL_Agent) | DQN agent playing Geometry Dash via screen capture and virtual input, with a custom environment loop — CPU-only | Reinforcement learning in a real game environment |
| [**markov-chatbot-cli**](https://github.com/zuroking/markov-chatbot-cli) | Command-line chatbot built on Markov chains and n-grams | Classical NLP before neural approaches |

## 🗺️ Roadmap

Extending the portfolio beyond ML foundations into systems programming, networking, and security.

```mermaid
flowchart LR
    A[ML foundations] --> B[Systems programming]
    B --> C[Networking & security]
    C --> D[AI Engineer]

    B --- B1[🔜 Terminal multiplexer]
    C --- C2[🔜 P2P file sync]
```

| Status | Next project | Goal |
|---|---|---|
| 🔜 | `terminal-multiplexer` | Build a tmux-like multiplexer with sessions and splits |
| 🔜 | `p2p-file-sync` | Build encrypted peer-to-peer file sync with chunk diffs and conflict resolution |

## ⚙️ Engineering principles

- 📐 Decide the architecture **before** writing implementation code — no "figure it out as I go".
- ✅ Enforce strict `mypy`, Pydantic v2 schemas, and Google-style docstrings.
- 🧪 Show real `pytest` output — never fabricated summaries.
- 🔍 Treat module-by-module review as a hard gate, not an afterthought.

---

<div align="center">

### 🤝 Let's build something meaningful

I'm looking for a Junior AI/ML Engineer opportunity — remote, hybrid, or on-site. If my projects resonate with you — or you know someone who's hiring — let's talk.

<a href="https://github.com/zuroking"><img src="https://img.shields.io/badge/Follow_on_GitHub-181717?style=for-the-badge&logo=github&logoColor=white" alt="Follow on GitHub" /></a>
<a href="https://t.me/Zuroking"><img src="https://img.shields.io/badge/Message_on_Telegram-26A5E4?style=for-the-badge&logo=telegram&logoColor=white" alt="Message on Telegram" /></a>

<img width="100%" src="https://capsule-render.vercel.app/api?type=waving&color=0:7C3AED,50:1D4ED8,100:0F172A&height=120&section=footer" />

</div>
