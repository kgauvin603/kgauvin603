# Keith Gauvin
### AI/ML Systems Architect • Enterprise Architect • Data Platform Engineer 

I design and ship **production-grade AI systems** that combine **LLMs, Retrieval-Augmented Generation (RAG), vector databases (ChromaDB), and cloud infrastructure**—with **evaluation, observability, and governance** as first-class concerns.

<a href="https://www.linkedin.com/in/keith-gauvin-63b2684/"><b>LinkedIn</b></a> •
<a href="mailto:keithggauvin@gmail.com"><b>keithggauvin@gmail.com</b></a> •
<a href="https://github.com/kgauvin603"><b>GitHub</b></a>

<img alt="banner" src="https://capsule-render.vercel.app/api?type=rect&color=0:0B1020,100:1F2A44&height=110&section=header&text=AI%20Architecture%20Portfolio%20%7C%20RAG%20%7C%20Agents%20%7C%20Cloud&fontSize=34&fontColor=E6EDF3&fontAlignY=45" />

</div>

---

## TL;DR
- **GenAI Architectures:** RAG, tool-use, multi-agent workflows, structured outputs
- **Data + Platform:** telemetry pipelines, enterprise data access patterns, vector search
- **Delivery:** portable cloud designs (incl. **GCP**) + containerization + CI/CD
- **Workflow:** prototype in **Google Colab / OCI Data Science** → harden into reusable repos and demos

---

## Tech (Badges)

<div align="center">

<img src="https://img.shields.io/badge/Python-0B1020?style=for-the-badge&logo=python&logoColor=white" />
<img src="https://img.shields.io/badge/SQL-0B1020?style=for-the-badge&logo=postgresql&logoColor=white" />
<img src="https://img.shields.io/badge/Agents-1F2A44?style=for-the-badge&logo=openai&logoColor=white" />
<img src="https://img.shields.io/badge/RAG-1F2A44?style=for-the-badge&logo=readthedocs&logoColor=white" />
<img src="https://img.shields.io/badge/ChromaDB-1F2A44?style=for-the-badge&logo=databricks&logoColor=white" />
<img src="https://img.shields.io/badge/Google%20Colab-1F2A44?style=for-the-badge&logo=googlecolab&logoColor=F9AB00" />
<img src="https://img.shields.io/badge/GCP-0B1020?style=for-the-badge&logo=googlecloud&logoColor=white" />

<img src="https://img.shields.io/badge/Docker-0B1020?style=for-the-badge&logo=docker&logoColor=white" />
<img src="https://img.shields.io/badge/Kubernetes-0B1020?style=for-the-badge&logo=kubernetes&logoColor=white" />
<img src="https://img.shields.io/badge/Terraform-0B1020?style=for-the-badge&logo=terraform&logoColor=7B42BC" />

</div>

---

## AI Architecture Map (How I build)

```mermaid
flowchart TB
  A[User / Product Need] --> B[Knowledge & Data]
  B --> C[Ingestion<br/>docs • telemetry • tables • files]
  C --> D[Retrieval Layer<br/>VectorDB • hybrid search • rerank]
  D --> E[Orchestration<br/>prompts • tools • agents]
  E --> F[Models<br/>LLM • embeddings • classifiers]
  F --> G[Apps<br/>API • notebook • UI]

  subgraph Trust[Trust & Governance]
    T1[PII / Sensitive Data Controls]
    T2[Prompt Injection Defenses]
    T3[Policy-Aware Tool Use]
    T4[Audit Logs]
  end

  subgraph Ops[Operations]
    O1[Observability<br/>traces • metrics • logs]
    O2[Evaluation<br/>golden sets • regression gates]
    O3[Cost / Latency Budgets]
    O4[Reliability<br/>fallbacks • retries • timeouts]
  end

  E --> Trust
  G --> Trust
  E --> Ops
  G --> Ops
```

---

## Reference System Diagram — RAG + Tools (cloud-portable, GCP included)

```mermaid
flowchart LR
  U[User] --> UI[Notebook / UI]
  UI --> ORCH[Orchestrator<br/>RAG + Tools + Policy]

  ORCH --> ING[Ingestion Jobs]
  ING --> OBJ[(Object Storage: OCI / GCS)]
  ING --> EMB[Embeddings]
  EMB --> VDB[(ChromaDB)]

  ORCH --> RET[Retriever]
  RET --> VDB
  RET --> DB[(Enterprise DB / Telemetry)]

  ORCH --> TOOL[Tools<br/>parsers • diagnostics • actions]
  TOOL --> ORCH

  ORCH --> LLM[LLM Runtime]
  LLM --> ORCH

  ORCH --> OBS[Observability]
  ORCH --> EVAL[Eval Harness]
  ORCH --> UI --> U
```

---

## Sample Projects (Curated)

<div align="center">

<a href="https://github.com/kgauvin603/IADP">
  <img src="https://github-readme-stats.vercel.app/api/pin/?username=kgauvin603&repo=IADP&theme=github_dark" />
</a>

<a href="https://github.com/kgauvin603/AgenticMigrationPlanner">
  <img src="https://github-readme-stats.vercel.app/api/pin/?username=kgauvin603&repo=AgenticMigrationPlanner&theme=github_dark" />
</a>

<a href="https://github.com/kgauvin603/23ai-SQL-Analyzer">
  <img src="https://github-readme-stats.vercel.app/api/pin/?username=kgauvin603&repo=23ai-SQL-Analyzer&theme=github_dark" />
</a>

<a href="https://github.com/kgauvin603/MyOracleProjects">
  <img src="https://github-readme-stats.vercel.app/api/pin/?username=kgauvin603&repo=MyOracleProjects&theme=github_dark" />
</a>

<a href="https://github.com/kgauvin603/kgauvin603_hf_repo">
  <img src="https://github-readme-stats.vercel.app/api/pin/?username=kgauvin603&repo=kgauvin603_hf_repo&theme=github_dark" />
</a>

<a href="https://github.com/kgauvin603/KeithGauvin-AI-ML-Python">
  <img src="https://github-readme-stats.vercel.app/api/pin/?username=kgauvin603&repo=KeithGauvin-AI-ML-Python&theme=github_dark" />
</a>

</div>

---

## What these projects demonstrate

### IADP — Integrated Agent Development Platform
A platform-style approach to building agentic systems:
- agent orchestration patterns
- tool interfaces + constraints
- repeatable workflows and extension points

### AgenticMigrationPlanner
A multi-step planning system designed around:
- decomposition (plan → research → execute)
- structured outputs
- traceability and guardrails

### 23ai-SQL-Analyzer
AI-assisted SQL/PLSQL analysis and correction:
- pattern detection + recommendations
- explainability and repeatable analysis flows
- engineering-friendly output formats

### MyOracleProjects
A curated set of AI/ML and RAG demos:
- end-to-end prototypes
- data + retrieval patterns
- notebook-driven experimentation

### Hugging Face Mirror (kgauvin603_hf_repo)
A practical bridge between:
- spaces/datasets artifacts
- reproducible experimentation
- model/data publishing workflows

### KeithGauvin-AI-ML-Python
Reusable reference code and learning assets:
- examples, utilities, and baseline patterns
- “from notebook to repo” structure

---

## Principles
- **Evaluation-driven iteration** (quality is measured, not guessed)
- **Security-by-design** (least privilege, secrets hygiene, safe tool use)
- **Production realism** (observability, cost/latency budgets, fallbacks)
- **Clear architectures** (diagrams, schemas, structured outputs)

---

## Contact
- **Email:** keithggauvin@gmail.com  
- **LinkedIn:** https://www.linkedin.com/in/keith-gauvin-63b2684/  
- **GitHub:** https://github.com/kgauvin603  



