<div>

# Lead Automation Engineer & AI Systems Architect 👋
### Deterministic Agentic Workflows - Infrastructure Reliability - n8n Expert

[![Linkedin Badge](https://img.shields.io/badge/-LinkedIn-0077B5?style=for-the-badge&logo=Linkedin&logoColor=white)](https://linkedin.com/in/ivangabrielmolina)
[![Mail Badge](https://img.shields.io/badge/-Email-D14836?style=for-the-badge&logo=Gmail&logoColor=white)](mailto:gabeesd06s@gmail.com)

<br>

<img src="https://readme-typing-svg.herokuapp.com?font=Fira+Code&weight=600&size=24&pause=900&color=336791&center=true&vCenter=true&width=700&lines=Architecting+Stateful+AI;Engineering+Deterministic+Agents;Building+Resilient+Systems;Zero+Trust+Automation" alt="Typing SVG" />

</div>

---

### 🚀 Engineering Philosophy
**Deterministic by Design.** I replace fragile linear scripts with intelligence-driven architectures. I build autonomous agents that operate within strict engineering guardrails. My work utilizes self-correction loops and state-machine logic to ensure data integrity and system observability in mission-critical environments.

---

<div>

### 🛠️ Technical Arsenal

| **🧠 AI & Reasoning** | **⚙️ Backend & Infra** | **⚡ Orchestration** |
| :---: | :---: | :---: |
| ![Ollama](https://img.shields.io/badge/Ollama-black?style=flat-square&logo=ollama&logoColor=white)<br>![DeepSeek](https://img.shields.io/badge/DeepSeek-R1-blue?style=flat-square)<br>![Qdrant](https://img.shields.io/badge/Qdrant-red?style=flat-square)<br>![Pydantic](https://img.shields.io/badge/Pydantic-E92063?style=flat-square&logo=pydantic&logoColor=white) | ![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)<br>![Node.js](https://img.shields.io/badge/Node.js-339933?style=flat-square&logo=node.js&logoColor=white)<br>![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)<br>![FastAPI](https://img.shields.io/badge/FastAPI-005571?style=flat-square&logo=fastapi&logoColor=white) | ![n8n](https://img.shields.io/badge/n8n-FF6560?style=flat-square&logo=n8n&logoColor=white)<br>![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white)<br>![Redis](https://img.shields.io/badge/Redis-DC382D?style=flat-square&logo=redis&logoColor=white)<br>![Git](https://img.shields.io/badge/Git-F05032?style=flat-square&logo=git&logoColor=white) |

</div>

---

<div>

## 🏆 High-Impact Projects (Technical Case Studies)

<br>

### 🎫 [LangKit: Agentic AI Ticket Intelligence](https://github.com/IGabrielMolina/LangKit)
**Engineering Focus:** Agentic Workflows, Service-Oriented Architecture (SOA), and Preventive Persistence.

A production-ready agentic orchestrator designed for local execution. This system mitigates LLM non-determinism through structural engineering.

* **Deterministic Orchestration:** Engineered a Directed Acyclic Graph (DAG) via `LangGraph` to manage feedback loops and autonomous self-correction.
* **Fault-Tolerant Persistence:** Implemented a **Write-Ahead Logging** (WAL) pattern with SQLite to ensure zero data loss during inference cycles.
* **Schema Enforcement:** Enforced rigid JSON outputs using `Pydantic` and Qwen 2.5 14B to eliminate hallucinations and ensure API compatibility.

```mermaid
sequenceDiagram
    actor U as User
    participant API as FastAPI
    participant DB as SQLite
    participant LG as LangGraph
    participant OLL as Ollama (Local)

    U->>API: POST /ticket JSON
    Note over API: Pydantic Validation
    API->>DB: INSERT ticket (Preventive Save)
    API->>LG: Start Graph (ticket_id + text)
    LG->>OLL: Structured Inference
    OLL-->>LG: Classified JSON
    LG->>DB: UPDATE ticket (Final State)
    LG-->>API: Result
    API-->>U: 200 Success
```

<br>

### 🚀 [Industrial-Grade Data Ingestion Pipeline](https://github.com/IGabrielMolina/stress-test-mkn)
**Engineering Focus:** Distributed Systems, Backpressure Management, and Fault Tolerance.

A high-scale pipeline built to handle massive telemetry spikes. The architecture decouples the ingestion layer to prevent database exhaustion.

* **Decoupled Architecture:** Utilized **Redis** as a message broker to separate API ingestion from heavy database writes.
* **Asynchronous Scaling:** Engineered isolated worker nodes to process high-volume loads in parallel without blocking the main gateway.

```mermaid
flowchart LR
    IoT([Python Simulator IoT])
    subgraph Ingestion Layer
        Gateway[n8n Main Gateway]
        Broker[(Redis Message Broker)]
    end
    subgraph Compute Cluster
        W_Alfa[Worker Alfa]
        W_Beta[Worker Beta]
    end
    subgraph Persistence Layer
        DB[(PostgreSQL)]
    end
    IoT --> Gateway --> Broker
    Broker --> W_Alfa & W_Beta
    W_Alfa & W_Beta --> DB
```

<br>

### 💳 [kitsu-fintech-engine: Autonomous Financial Pipeline](https://github.com/IGabrielMolina/kitsu-fintech-engine)
**Engineering Focus:** Protocol Bridging, Asynchronous Scaling, and Deterministic Validation.

High-performance middleware integrating legacy financial protocols with modern REST API architecture.

* **Protocol Integration:** Designed a seamless bridge between IMAP/SMTP legacy data and a modern backend.
* **Human-in-the-Loop (HITL):** Implemented risk-aware routing that triggers Slack-based approvals for high-value transactions before database commitment.

<br>

### 🦊 [Kitsu_Agent: Sovereign On-Premise AI Orchestrator](https://github.com/IGabrielMolina/Kitsu_agent)
**Engineering Focus:** Security, Observability, and Data Sovereignty.

A secure AI orchestration engine featuring metadata-based RBAC. Designed for zero-egress environments where data privacy is mandatory. It runs `DeepSeek-R1` locally via Ollama to ensure absolute data sovereignty.

---

<div>
  <p>📍 Based in Argentina (UTC-3) 🇦🇷</p>
  <p>🌍 Optimized for EMEA/UK/US business hours</p>
  <p>🚀 Open for Global Engineering Opportunities</p>
</div>
