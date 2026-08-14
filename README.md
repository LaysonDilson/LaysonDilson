<h1 align="center">Layson Dilson Souza Santos</h1>
<p align="center"><b>AI Engineer &nbsp;|&nbsp; Software Architect</b></p>
<p align="center">
  13+ years building distributed systems in Java — now building systems<br>
  where the LLM is <i>part of the architecture</i>, not a chatbot bolted on top.<br>
  Rio de Janeiro, Brazil
</p>

<p align="center">
  <b>🟢 Available for contract work</b> — part-time allocation (2–3 days/week) or fixed-scope projects
</p>

<p align="center">
  <a href="https://www.linkedin.com/in/laysondilson"><img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=flat&logo=linkedin&logoColor=white" alt="LinkedIn"></a>
  &nbsp;
  <a href="mailto:laysondilson@gmail.com"><img src="https://img.shields.io/badge/Email-D14836?style=flat&logo=gmail&logoColor=white" alt="Email"></a>
</p>

---

## What I do

I design and run **AI-native systems in production** — not demos. The distinction that matters: my day
job is an operation with real money in it, and the software that runs it is software I built.

- **MCP servers as a product surface.** A 35-tool Model Context Protocol server that gives an LLM agent
  read *and* write access to a live manufacturing operation: order ingestion from two marketplaces,
  production scheduling against shipping deadlines, FIFO material costing. Used every day. A public
  reference implementation of the architecture is below.
- **Self-hosted AI pipelines.** GPU-backed containers running `faster-whisper large-v3` and programmatic
  video rendering, orchestrated in n8n, at a marginal cost of about R$0.47 per finished piece.
- **Protocol-level integration.** A heterogeneous fleet of 3D printers behind adapters for HTTP REST,
  WebSocket, and MQTT-over-TLS + FTPS, bridged into an event-driven automation layer.
- **The Java underneath.** Fintech, streaming, and e-commerce at scale — 10k+ req/s, 99.99% uptime,
  event-driven architectures, and the migrations nobody volunteers for.

The combination is the point: most people doing LLM work have never run a system under load, and most
people who have run systems under load treat AI as autocomplete.

---

## Featured

### [mcp-ops-server](https://github.com/LaysonDilson/mcp-ops-server) · public reference implementation

An MCP server giving an LLM agent **safe write access** to a real operations database. ~1,000 lines,
11 tools, 29 tests, runnable demo. It exists to show the four rules that make agent-facing data survive
contact with reality:

- order status is **derived** from its items, never assigned — there is no code path where an agent marks
  unproduced work as ready
- re-importing a channel export **preserves production progress** instead of resetting it
- header-level money is read **once per order**, never summed per line
- stock balance is a **sum over an append-only log**, never a stored counter

Plus a section on why tool docstrings are the entire interface contract a model sees — and what happens
when they are written carelessly.

### Rowdz · founder & architect · 2025–2026

Multi-tenant B2B SaaS, designed, built, shipped and operated end-to-end solo. Discontinued in 2026 —
listed here for the engineering, which is the part that transfers.

- Strict tenant isolation via `TenantContext` (ThreadLocal), enforced at every repository query
- Production migration **PostgreSQL → MongoDB** in 11 incremental phases, dual-write, zero downtime
- OAuth 2.0, AES-256-GCM token encryption at rest, HMAC webhook validation
- Domain-Driven Design with bounded contexts and domain events
- 248 automated tests (unit + integration via Testcontainers) → GitHub Actions → Cloud Run

**Stack:** Java 21 · Spring Boot 3 · React + TypeScript · MongoDB Atlas · GCP Cloud Run

---

## Tech Stack

**AI & Automation**
<p>
  <img src="https://img.shields.io/badge/MCP-000000?style=flat&logo=anthropic&logoColor=white">
  <img src="https://img.shields.io/badge/n8n-EA4B71?style=flat&logo=n8n&logoColor=white">
  <img src="https://img.shields.io/badge/OpenAI-412991?style=flat&logo=openai&logoColor=white">
  <img src="https://img.shields.io/badge/Whisper-000000?style=flat&logo=openai&logoColor=white">
  <img src="https://img.shields.io/badge/FastAPI-009688?style=flat&logo=fastapi&logoColor=white">
  <img src="https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white">
</p>

**Languages**
<p>
  <img src="https://img.shields.io/badge/Java-007396?style=flat&logo=openjdk&logoColor=white">
  <img src="https://img.shields.io/badge/Kotlin-7F52FF?style=flat&logo=kotlin&logoColor=white">
  <img src="https://img.shields.io/badge/TypeScript-3178C6?style=flat&logo=typescript&logoColor=white">
  <img src="https://img.shields.io/badge/Node.js-339933?style=flat&logo=node.js&logoColor=white">
</p>

**Frameworks & Runtimes**
<p>
  <img src="https://img.shields.io/badge/Spring%20Boot-6DB33F?style=flat&logo=spring-boot&logoColor=white">
  <img src="https://img.shields.io/badge/Quarkus-4695EB?style=flat&logo=quarkus&logoColor=white">
  <img src="https://img.shields.io/badge/React-61DAFB?style=flat&logo=react&logoColor=black">
</p>

**Cloud & Infrastructure**
<p>
  <img src="https://img.shields.io/badge/Google%20Cloud-4285F4?style=flat&logo=googlecloud&logoColor=white">
  <img src="https://img.shields.io/badge/AWS-232F3E?style=flat&logo=amazonaws&logoColor=white">
  <img src="https://img.shields.io/badge/Docker-2496ED?style=flat&logo=docker&logoColor=white">
  <img src="https://img.shields.io/badge/Kubernetes-326CE5?style=flat&logo=kubernetes&logoColor=white">
  <img src="https://img.shields.io/badge/Argo%20CD-EF7B4D?style=flat&logo=argo&logoColor=white">
</p>

**Event-Driven & Messaging**
<p>
  <img src="https://img.shields.io/badge/Apache%20Kafka-231F20?style=flat&logo=apache-kafka&logoColor=white">
  <img src="https://img.shields.io/badge/Pub%2FSub-4285F4?style=flat&logo=googlecloud&logoColor=white">
  <img src="https://img.shields.io/badge/RabbitMQ-FF6600?style=flat&logo=rabbitmq&logoColor=white">
  <img src="https://img.shields.io/badge/MQTT-660066?style=flat&logo=mqtt&logoColor=white">
</p>

**Databases**
<p>
  <img src="https://img.shields.io/badge/PostgreSQL-4169E1?style=flat&logo=postgresql&logoColor=white">
  <img src="https://img.shields.io/badge/MongoDB-47A248?style=flat&logo=mongodb&logoColor=white">
  <img src="https://img.shields.io/badge/Redis-DC382D?style=flat&logo=redis&logoColor=white">
  <img src="https://img.shields.io/badge/DynamoDB-4053D6?style=flat&logo=amazondynamodb&logoColor=white">
  <img src="https://img.shields.io/badge/SQLite-003B57?style=flat&logo=sqlite&logoColor=white">
</p>

**Observability & Quality**
<p>
  <img src="https://img.shields.io/badge/Datadog-632CA6?style=flat&logo=datadog&logoColor=white">
  <img src="https://img.shields.io/badge/Dynatrace-1496FF?style=flat&logo=dynatrace&logoColor=white">
  <img src="https://img.shields.io/badge/Grafana-F46800?style=flat&logo=grafana&logoColor=white">
  <img src="https://img.shields.io/badge/Prometheus-E6522C?style=flat&logo=prometheus&logoColor=white">
  <img src="https://img.shields.io/badge/SonarQube-4E9BCD?style=flat&logo=sonarqube&logoColor=white">
</p>

---

## Career

| Period | Company | Role |
|---|---|---|
| **Aug 2025 – Present** | **print3dlm** | Founder — operating a manufacturing business on software I build |
| Feb 2026 – Jul 2026 | PicPay | Senior Software Engineer |
| Mar 2025 – Aug 2025 | CI&T (Bradesco) | Senior Architect |
| Nov 2024 – Jan 2025 | Invillia (iFood) | Senior Software Engineer |
| Nov 2022 – Nov 2024 | NTConsult (GloboPlay) | Senior Software Engineer |
| Jan 2021 – Nov 2022 | Niky | Java Architect |
| May 2019 – Dec 2020 | GFT (Santander) | Java Architect |
| Jun 2016 – May 2019 | Zup Innovation | Senior Java Developer |

BSc Computer Science, Universidade Federal de Uberlândia · Portuguese (native), English (professional working proficiency)

---

## Working together

Three formats, whichever fits:

| Format | What it looks like |
|---|---|
| **Part-time allocation** | 2–3 days a week as technical reinforcement for your team — no hiring overhead |
| **Fixed-scope project** | Integration, automation, data migration, importer. Defined scope, price and deadline |
| **Advisory** | Architecture review, technical decision support, code review |

Where I add the most value right now: **connecting a system you already have to an agent that can query
and act on it** — safely, with an audit trail, and without a rewrite.

📬 [laysondilson@gmail.com](mailto:laysondilson@gmail.com) · [LinkedIn](https://www.linkedin.com/in/laysondilson)

---

<p align="center"><i>"Build it well, document it clearly, and leave the codebase better than you found it."</i></p>
