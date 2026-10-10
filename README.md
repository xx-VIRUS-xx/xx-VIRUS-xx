<h1 align="center">Hey, I'm Prabhat 👋</h1>
<h3 align="center">AI engineer building agentic systems and retrieval infrastructure</h3>

<p align="center">
  <a href="https://www.linkedin.com/in/prabhat-saxena-154529191"><img src="https://img.shields.io/badge/LinkedIn-Connect-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn"></a>
  <a href="mailto:pm10182000@gmail.com"><img src="https://img.shields.io/badge/Email-Contact-D14836?style=for-the-badge&logo=gmail&logoColor=white" alt="Email"></a>
  <a href="https://github.com/xx-VIRUS-xx?tab=repositories"><img src="https://img.shields.io/badge/GitHub-Repositories-181717?style=for-the-badge&logo=github&logoColor=white" alt="Repositories"></a>
  <a href="https://x.com/xxVirusxx2801"><img src="https://img.shields.io/badge/X-Follow-000000?style=for-the-badge&logo=x&logoColor=white" alt="X"></a>
  <a href="https://leetcode.com/u/xVirusx/"><img src="https://img.shields.io/badge/LeetCode-Profile-FFA116?style=for-the-badge&logo=leetcode&logoColor=white" alt="LeetCode"></a>
  <a href="https://www.hackerrank.com/profile/pm10182000"><img src="https://img.shields.io/badge/HackerRank-Profile-00EA64?style=for-the-badge&logo=hackerrank&logoColor=white" alt="HackerRank"></a>
</p>

---

### About

I lead an AI engineering team in India. B.Tech in Computer Engineering (2021), and I earned the AWS Developer – Associate and Database – Specialty certifications in 2022 (both since expired, see below). My work sits where LLM applications meet infrastructure: retrieval and memory for agents, local LLM inference, and the queues, search clusters and services that keep them running in production.

On the side I do research and publish it **with the failures included**: each experiment has a design doc and a results doc, and negative results stay in.

### What I'm into

- **Retrieval for code and agents**: BM25, dense, hybrid and graph-based retrieval, and how to measure whether any of it helps
- **Persistent memory for LLM agents**: structured, auditable memory instead of ever-longer context windows
- **LLM infrastructure**: local inference (Ollama, SGLang, vLLM), gateways with caching, fallback and cost tracking
- **Distributed systems**: Elasticsearch, Kafka, Celery, Redis, PostgreSQL, Kubernetes
- **Privacy-minded AI tooling**: PII masking, encrypted storage, audit trails, human-in-the-loop design

### Certifications

<p>
  <a href="https://www.credly.com/badges/201b1ea0-1d66-4403-87d3-c6dbd2b17826"><img src="https://images.credly.com/images/b9feab85-1a43-4f6c-99a5-631b88d5461b/image.png" alt="AWS Certified Developer – Associate" height="120"></a>
  <a href="https://www.credly.com/badges/e06c12c3-ee70-406e-9f50-0bd8890c21dc"><img src="https://images.credly.com/images/885d38e4-55c0-4c35-b4ed-694e2b26be6c/image.png" alt="AWS Certified Database – Specialty" height="120"></a>
</p>

- **AWS Certified Developer – Associate**: issued May 2022, expired May 2025 · [verify on Credly](https://www.credly.com/badges/201b1ea0-1d66-4403-87d3-c6dbd2b17826)
- **AWS Certified Database – Specialty**: issued Oct 2022, expired Oct 2025 · [verify on Credly](https://www.credly.com/badges/e06c12c3-ee70-406e-9f50-0bd8890c21dc)

---

### Research

**[CodeGraph-TACM](https://github.com/xx-VIRUS-xx/CodegraphTACM)** · *Topology-Aware Context Manager: retrieval for coding agents*
A resolver that scores files, classes and functions from several graph signals and packs the best ones into a fixed token budget, compared against BM25, dense and hybrid retrieval over six experiments.
- On 47 SWE-bench Lite and Multilingual Python instances, density-gated personalised PageRank reached **Hit@5 36.2% vs 27.7%** for a BM25 + MiniLM hybrid, at no ML inference cost. MRR (0.198 vs 0.192) stays inside the confidence intervals, and the write-up says so.
- Includes the negative results, for example query-side identifier expansion gave no improvement at any tested scale.

**[N-Dimensional Memory](https://github.com/xx-VIRUS-xx/N-Dimensional-Memory)** · *an external memory for LLM agents*
An LLM extracts entities per turn; a deterministic engine owns identity, time, attribution and what counts as a fact versus a claim, then builds a short question-specific view for the answering model.
- Strongest where retrieval is weakest: speaker attribution (7/8 vs 5/8 for reading the raw text on false-premise questions) and dates (7/7 temporal questions).
- At equal size it only **tied BM25** retrieval, so the project is documented and closed as a negative result.

---

### Selected projects

| Project | What it is |
|---|---|
| [**gdpr-llm-proxy**](https://github.com/xx-VIRUS-xx/gdpr-llm-proxy) | Proxy that masks personal data before an LLM call leaves the EU and restores it in the response. Presidio detection, Fernet-encrypted token store with TTL, 55 tests |
| [**euaiact-compliance**](https://github.com/xx-VIRUS-xx/euaiact-compliance) | EU AI Act risk-tier classifier: rules decide the tier, retrieved regulation text (Qdrant) justifies it, every decision is audit-logged |
| [**vscars-public**](https://github.com/xx-VIRUS-xx/vscars-public) | VSCARS (beta): a cloud relay plus CLI that lets you use your own dev machine, with terminal, files, git and AI chat, from a phone or any browser. This repo holds the docs and the installer |
| [**Declutter**](https://github.com/xx-VIRUS-xx/Declutter) | Chrome extension that hides page clutter and remembers your choices per site, with zero network calls |

Also worth a look: [**practice-ops-agent**](https://github.com/xx-VIRUS-xx/practice-ops-agent) (multi-tenant clinic back office with field-level encryption and human-approved AI actions) and [**LNSBotz**](https://github.com/xx-VIRUS-xx/LNSBotz) (FastAPI platform of AI utilities with a model gateway, Celery workers and payments).

More prototypes, system-design notes and experiments are in [my repositories](https://github.com/xx-VIRUS-xx?tab=repositories). Each README says plainly what works and what does not.

---

### Tech stack

<p align="left">
  <img src="https://skillicons.dev/icons?i=python,fastapi,django,postgres,redis,kafka,elasticsearch,docker,kubernetes,aws,grafana,pytorch,typescript,linux,git,go,javascript" alt="Tech stack" />
</p>

`LangChain` `LangGraph` `LlamaIndex` `RAG / GraphRAG` `Qdrant` `FAISS` `Ollama` `SGLang` `vLLM` `Celery` `OpenTelemetry`

---

### Currently

- Extending CodeGraph-TACM toward session-level subgraphs (design in the repo)
- Writing up what did and did not work in agent memory
- Shipping small, well-documented tools with tests

<p align="center"><sub>Open to conversations about retrieval, agent memory and LLM infrastructure.</sub></p>
