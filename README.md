<div>

# Hi there, I'm Gabriel Molina 👋
### AI Systems Architect | Deterministic Agentic Workflows | Builder

[![Linkedin Badge](https://img.shields.io/badge/-LinkedIn-0077B5?style=for-the-badge&logo=Linkedin&logoColor=white)](https://linkedin.com/in/ivangabrielmolina)
[![Mail Badge](https://img.shields.io/badge/-Email-D14836?style=for-the-badge&logo=Gmail&logoColor=white)](mailto:gabeesd06s@gmail.com)

<br>
<br>

<img src="https://readme-typing-svg.herokuapp.com?font=Fira+Code&weight=600&size=24&pause=1000&color=336791&center=true&vCenter=true&width=700&lines=Architecting+Stateful+AI+Systems;Closing+the+Loop:+Know+->+Do+->+Reflect;Engineering+Deterministic+Agents" alt="Typing SVG" />

</div>

---

### 🚀 Engineering Philosophy
> *I build systems that are Deterministic by Design. I thrive at the intersection of creative problem-solving and rigorous engineering, moving beyond linear scripts to create **intelligence-driven architectures**. Whether it's a local LLM reasoning engine or an event-driven orchestrator, my focus is on building agents that actually close the loop—reflecting and adjusting based on real outcomes—while ensuring 100% data integrity.*

---

<div>

### 🛠️ Technical Arsenal

| **🧠 The Brain (AI)** | **⚙️ The Engine (Backend)** | **⚡ The Logic (Orch)** |
| :---: | :---: | :---: |
| ![Ollama](https://img.shields.io/badge/Ollama-black?style=flat-square&logo=ollama&logoColor=white)<br>![DeepSeek](https://img.shields.io/badge/DeepSeek-R1-blue?style=flat-square)<br>![Qdrant](https://img.shields.io/badge/Qdrant-red?style=flat-square) | ![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)<br>![Node.js](https://img.shields.io/badge/Node.js-339933?style=flat-square&logo=node.js&logoColor=white)<br>![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white) | ![n8n](https://img.shields.io/badge/n8n-FF6560?style=flat-square&logo=n8n&logoColor=white)<br>![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white)<br>![Git](https://img.shields.io/badge/Git-F05032?style=flat-square&logo=git&logoColor=white) |

</div>

---

<div>

## 🏆 High-Impact Projects (The Sandbox)

<br>
<div>

### 🎫 [LangKit: Agentic AI Ticket Intelligence](https://github.com/IGabrielMolina/LangKit)

> **Engineering Focus:** Agentic Workflows, Service-Oriented Architecture (SOA), and Preventive Persistence.

</div>

A production-ready **Agentic Orchestrator** combining decoupled services with state-machine AI logic for local, privacy-first execution.

**Agentic Orchestration:** Engineered a Directed Acyclic Graph (DAG) using `LangGraph` to handle complex LLM feedback loops and self-correction cycles, effectively **closing the loop** on non-deterministic AI outputs.

**Service-Oriented Architecture (SOA):** Separated inference (local Ollama), business logic (FastAPI), and frontend (Streamlit) into isolated, dockerized containers to ensure system resilience.

**Preventive Persistence:** Implemented a Write-Ahead Logging pattern with SQLite to guarantee zero data loss during unpredictable LLM inference failures or hardware limits.

**Strict Deterministic Validation:** Enforced highly structured JSON outputs leveraging `Pydantic` and Qwen 2.5 14B, eliminating hallucinated formatting and ensuring API compliance.

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

<div>

![Python](https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white) ![LangGraph](https://img.shields.io/badge/LangGraph-DD0031?style=flat) ![FastAPI](https://img.shields.io/badge/FastAPI-005571?style=flat&logo=fastapi&logoColor=white) ![Ollama](https://img.shields.io/badge/Ollama-black?style=flat&logo=ollama&logoColor=white) ![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat&logo=docker&logoColor=white)

</div>

<br>

<br>

<br>

### 🚀 [Industrial-Grade Data Ingestion Pipeline](https://github.com/IGabrielMolina/stress-test-mkn)

> **Engineering Focus:** Distributed Systems, Backpressure Management, and Fault Tolerance.

</div>

A highly scalable, fault-tolerant **Proof of Concept (PoC)** designed to handle massive telemetry data spikes without data loss or gateway timeouts.

**Decoupled Architecture:** Engineered a queue-based system utilizing a message broker to separate API ingestion from database writing, effectively mitigating backpressure during traffic spikes.

**Horizontal Scalability:** Deployed a cluster of isolated worker nodes capable of asynchronously processing high-volume loads (e.g., IoT sensors, bulk ERP migrations) without crashing the main gateway.

**Real-Time Telemetry:** Implemented a live monitoring dashboard to track cluster health, worker distribution, and database write metrics in real-time.


```mermaid
flowchart LR
    %% External Nodes
    IoT([Python Simulator IoT])

    %% Layers
    subgraph Ingestion Layer
        Gateway[n8n Main Gateway]
        Broker[(Redis Message Broker)]
    end

    subgraph Compute Cluster
        W_Alfa[Worker Alfa]
        W_Beta[Worker Beta]
        W_Gama[Worker Gama]
    end

    subgraph Persistence Layer
        DB[(PostgreSQL)]
    end

    subgraph Output Layer
        Dash[MKN OS]
    end

    %% Flow execution
    IoT -->|Incoming Data| Gateway
    Gateway -->|Queue Push| Broker

    Broker -->|JS Data Cleaning & Tagging| W_Alfa
    Broker -->|JS Data Cleaning & Tagging| W_Beta
    Broker -->|JS Data Cleaning & Tagging| W_Gama

    W_Alfa -->|Async Write| DB
    W_Beta -->|Async Write| DB
    W_Gama -->|Async Write| DB

    DB -.->|Cloudflare Tunnel| Dash
```

<div>

![n8n](https://img.shields.io/badge/n8n-FF6560?style=flat&logo=n8n&logoColor=white) ![Redis](https://img.shields.io/badge/Redis-DC382D?style=flat&logo=redis&logoColor=white) ![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat&logo=postgresql&logoColor=white) ![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat&logo=docker&logoColor=white) ![Python](https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white)

</div>

<br>

### 💳 [kitsu-fintech-engine: Autonomous Financial Pipeline](https://github.com/IGabrielMolina/kitsu-fintech-engine)

> **Engineering Focus:** Protocol Bridging, Asynchronous Scaling, and Deterministic Validation.

</div>

A high-performance **Middleware & ETL Pipeline** that bridges legacy protocols with modern AI-driven orchestration.

**Legacy-to-Modern Bridge:** Engineered a seamless integration between legacy mail protocols (IMAP/SMTP via SMTP4dev) and a modern REST API architecture.

**Async Middleware:** Developed a FastAPI backend that orchestrates local LLM inference (Qwen 2.5 14B) using non-blocking `async/await` logic for real-time document auditing.

**Human-in-the-Loop (HITL):** Implemented a risk-aware routing system that triggers Slack-based manual approvals for transactions >$4,000 before committing to PostgreSQL.

**Resilient Persistence:** Optimized SQL schema with custom `Check Constraints` to ensure data integrity across the entire ingestion lifecycle.

<div>

![Python](https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white) ![FastAPI](https://img.shields.io/badge/FastAPI-005571?style=flat&logo=fastapi) ![n8n](https://img.shields.io/badge/n8n-FF6560?style=flat&logo=n8n&logoColor=white) ![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat&logo=postgresql&logoColor=white)

</div>

<br>
<br>

<div>

### 🦊 [Kitsu_Agent: Sovereign On-Premise AI Orchestrator](https://github.com/IGabrielMolina/Kitsu_agent)
[![Demos Included](https://img.shields.io/badge/🎥_Live_Demos_Inside-FF0000?style=flat-square&logo=youtube&logoColor=white)](https://github.com/IGabrielMolina/Kitsu_agent)

> **Engineering Focus:** Security, Observability, and Data Sovereignty.

</div>

A secure **AI Orchestration Engine** featuring metadata-based RBAC and self-healing logic.

**Zero-Egress:** Runs `DeepSeek-R1` locally via Ollama. No data leaves the server.

**Audit Trail:** Implemented real-time telemetry in PostgreSQL (Confidence Scores & Latency).

**Security:** Deterministic RBAC ensuring users only access authorized vectors in Qdrant.

<div>
  
![Python](https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white) ![n8n](https://img.shields.io/badge/n8n-FF6560?style=flat&logo=n8n&logoColor=white) ![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat&logo=docker&logoColor=white)

</div>

<br>
<br>

<div>

### ⚡ [python-zoho-crm-bridge: Event-Driven CRM Middleware](https://github.com/IGabrielMolina/python-zoho-crm-bridge)

> **Engineering Focus:** Event-Driven Architecture, Data Validation, and Enterprise Integration.

</div>

A robust, multi-layered middleware pipeline synchronizing real-time database events into external CRM platforms.

**Event-Driven Orchestration:** Engineered a decoupled flow where a Node.js backend writes to PostgreSQL, which is passively monitored by an n8n orchestration layer to detect state changes in real-time.

**Strict Payload Validation:** Developed a Python endpoint acting as a secure gateway, leveraging `Pydantic` for rigorous data validation and sanitization before processing external requests.

**Automated CRM Injection:** Translates normalized database events into structured API calls, autonomously inserting validated leads into Zoho CRM without human intervention.

**Scalable Separation of Concerns:** Microservice-oriented design isolating database writes (Node.js), event routing (n8n), and API validation/execution (Python).

<div>

![Python](https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white) ![Node.js](https://img.shields.io/badge/Node.js-339933?style=flat&logo=node.js&logoColor=white) ![FastAPI](https://img.shields.io/badge/FastAPI-005571?style=flat&logo=fastapi) ![n8n](https://img.shields.io/badge/n8n-FF6560?style=flat&logo=n8n&logoColor=white) ![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat&logo=postgresql&logoColor=white)

</div>

---

<div>
  <p>Currently based in Argentina (UTC-3) 🇦🇷</p>
  <p>Open for Global Engineering Opportunities</p>
</div>
