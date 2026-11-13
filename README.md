<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:0d1117,50:1f6feb,100:70a5fd&height=210&section=header&text=Yash%20Bhosale&fontColor=ffffff&fontSize=54&fontAlignY=36&desc=AI%20Engineer%20%C2%B7%20RAG%20%C2%B7%20Agents%20%C2%B7%20LLM%20Evaluation&descSize=19&descAlignY=58&animation=fadeIn" width="100%" alt="Yash Bhosale: AI Engineer working on RAG, agents and LLM evaluation" />

<a href="https://git.io/typing-svg">
  <img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=500&size=21&duration=2800&pause=900&color=70A5FD&center=true&vCenter=true&width=760&lines=RAG+systems+that+cite+their+sources%2C+or+abstain;Measured%2C+not+claimed%3A+evals+before+opinions;LangGraph+agents+%C2%B7+hybrid+retrieval+%C2%B7+LLM+judges;From+notebook+to+production+on+AWS" alt="RAG systems that cite their sources, or abstain. Measured, not claimed. LangGraph agents, hybrid retrieval, LLM judges. From notebook to production on AWS." />
</a>

<p>
  <a href="mailto:bhosaleyash789@gmail.com"><img src="https://img.shields.io/badge/Email-D14836?style=for-the-badge&logo=gmail&logoColor=white" alt="Email" /></a>
  <a href="https://linkedin.com/in/yashbhosale789"><img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logoColor=white" alt="LinkedIn" /></a>
  <a href="https://yash-pkb-rag.duckdns.org"><img src="https://img.shields.io/badge/Live_demo-Personal_Knowledge_OS-1f6feb?style=for-the-badge" alt="Live demo of Personal Knowledge OS" /></a>
</p>

</div>

## 🧠 About me

I'm an AI Engineer. I build retrieval and agent systems and I care most about one question: **how do you know it works?** So every quality claim on this page comes from a versioned dataset, and every change is checked with a paired comparison before it ships.

- 🚀 **Shipped** [Personal Knowledge OS](https://github.com/yashbhosale789/Personal-Knowledge-RAG): a production RAG system, live on AWS on a $0 budget, with CI/CD, tracing, SLOs and alerting.
- 📏 **Wrote** [rag-eval-kit](https://github.com/yashbhosale789/rag-eval-kit) so any RAG system can be scored the same way: retrieval metrics, a calibrated LLM judge and paired statistics.
- 🧪 **Benchmarked** four RAG designs on one corpus and one question set in [rag-benchmarks](https://github.com/yashbhosale789/rag-benchmarks).
- 🤖 **Building** LangGraph agents with corrective retrieval, graders, knowledge-graph expansion and guardrails.

## 🚀 Featured work

<table>
  <tr>
    <td width="50%" valign="top">
      <h3>🧠 <a href="https://github.com/yashbhosale789/Personal-Knowledge-RAG">Personal Knowledge OS</a></h3>
      <p><strong>Production RAG: a cited answer, or an honest "the documents don't say".</strong></p>
      <p>
        <a href="https://github.com/yashbhosale789/Personal-Knowledge-RAG/actions/workflows/tests.yml"><img src="https://github.com/yashbhosale789/Personal-Knowledge-RAG/actions/workflows/tests.yml/badge.svg" alt="Tests" /></a>
        <a href="https://github.com/yashbhosale789/Personal-Knowledge-RAG"><img src="https://img.shields.io/github/stars/yashbhosale789/Personal-Knowledge-RAG?style=flat&color=70a5fd" alt="GitHub stars" /></a>
        <a href="https://yash-pkb-rag.duckdns.org"><img src="https://img.shields.io/badge/demo-live-2ea043?style=flat" alt="Live demo" /></a>
      </p>
      <ul>
        <li>Dense + BM25 retrieval, reciprocal rank fusion, cross-encoder reranking: <strong>Recall@3 0.88, MRR 0.83</strong> on 236 PDFs</li>
        <li>A sufficiency gate abstains when the evidence is missing; a second model family verifies every citation</li>
        <li>Redis semantic cache, streamed answers (SSE), React + TypeScript UI</li>
        <li>Runs on a 2 GiB AWS EC2 instance: deploy on merge with health checks and automatic rollback, Prometheus + Grafana SLOs, Langfuse traces, an LLM-judge regression gate in CI</li>
      </ul>
      <p><code>FastAPI</code> <code>ChromaDB</code> <code>Redis</code> <code>React</code> <code>Docker</code> <code>AWS</code> <code>GitHub Actions</code></p>
    </td>
    <td width="50%" valign="top">
      <h3>📏 <a href="https://github.com/yashbhosale789/rag-eval-kit">rag-eval-kit</a></h3>
      <p><strong>Measure any RAG system through a small adapter.</strong></p>
      <p>
        <a href="https://github.com/yashbhosale789/rag-eval-kit/actions/workflows/tests.yml"><img src="https://github.com/yashbhosale789/rag-eval-kit/actions/workflows/tests.yml/badge.svg" alt="Tests" /></a>
        <a href="https://github.com/yashbhosale789/rag-eval-kit/tags"><img src="https://img.shields.io/github/v/tag/yashbhosale789/rag-eval-kit?style=flat&color=70a5fd&label=version" alt="Latest version" /></a>
      </p>
      <ul>
        <li>Two methods, <code>retrieve()</code> and <code>answer()</code>, are all the kit needs to know about your system</li>
        <li>Recall@k, success@k and MRR with no LLM calls; an LLM judge for faithfulness, correctness and relevancy, with a calibration check for the judge itself</li>
        <li><code>compare</code> runs a paired bootstrap CI and a sign test, so you can tell a real gain from noise</li>
        <li><code>gate</code> fails CI on a regression; runs resume where they stopped, which suits free-tier quotas</li>
      </ul>
      <p><code>Python</code> <code>CLI</code> <code>dependency-free core</code> <code>any OpenAI-compatible judge</code></p>
    </td>
  </tr>
  <tr>
    <td width="50%" valign="top">
      <h3>🖼️ <a href="https://github.com/yashbhosale789/multimodal-rag">multimodal-rag</a></h3>
      <p><strong>An agentic chatbot that reads charts and follows facts across documents.</strong></p>
      <ul>
        <li>A vision model transcribes every chart and diagram, so numbers that only exist as a bar in a chart are answerable</li>
        <li>Neo4j knowledge graph with one-hop expansion: multi-hop questions went from 0/2 to 2/2 on its answer key</li>
        <li>LangGraph corrective loop: grade the hits, then rewrite, search the web or answer from model knowledge</li>
        <li>Prompt-injection guard, PII masking, audit log, Langfuse tracing</li>
      </ul>
      <p><code>LangGraph</code> <code>Pinecone</code> <code>Neo4j</code> <code>Gemini</code> <code>FastAPI</code> <code>Streamlit</code> <code>Docker</code></p>
    </td>
    <td width="50%" valign="top">
      <h3>🤖 <a href="https://github.com/yashbhosale789/agentic-rag">agentic-rag</a></h3>
      <p><strong>A LangGraph ReAct agent that writes its own searches.</strong></p>
      <ul>
        <li>Built as an explicit state graph: <code>agent → tools → grade → agent</code></li>
        <li>A grader checks each retrieval and sends the agent back to search again when the chunks miss (corrective RAG)</li>
        <li>Bounded to 6 steps; graph routing is tested with a stubbed LLM, no API key needed</li>
      </ul>
      <p><code>LangGraph</code> <code>LangChain</code> <code>Groq</code> <code>ChromaDB</code> <code>BM25</code></p>
      <p>Part of a ladder of variants: <a href="https://github.com/yashbhosale789/naive-rag">naive-rag</a> → <a href="https://github.com/yashbhosale789/advanced-rag">advanced-rag</a> → agentic-rag → Personal Knowledge OS.</p>
    </td>
  </tr>
</table>

## 📊 Measured, not claimed

Four RAG designs, one corpus (236 PDFs), one set of 71 labelled questions, one code path ([rag-eval-kit](https://github.com/yashbhosale789/rag-eval-kit)):

| Variant | Retrieval | Recall@3 | MRR |
| --- | --- | :---: | :---: |
| [Naive RAG](https://github.com/yashbhosale789/naive-rag) | dense top-k | 0.655 | 0.594 |
| [Advanced RAG](https://github.com/yashbhosale789/advanced-rag) | dense + BM25 → RRF → cross-encoder rerank | 0.742 | 0.735 |
| [Agentic RAG](https://github.com/yashbhosale789/agentic-rag) (retrieve tool) | same pipeline, called by an agent | 0.742 | 0.735 |
| [Production RAG](https://github.com/yashbhosale789/Personal-Knowledge-RAG) | + LLM query rewrite, larger chunks, top 3 | **0.876** | **0.829** |

Production's Recall@3 gain over Advanced holds up under a paired bootstrap and a sign test. The run files, the settings that differ and the differences that did *not* hold up are in [rag-benchmarks](https://github.com/yashbhosale789/rag-benchmarks).

<details>
<summary><strong>How the production pipeline answers a question</strong></summary>

```mermaid
flowchart LR
    Q(["Question"]) --> C{"Semantic<br/>cache"}
    C -- hit --> A(["Cited answer"])
    C -- miss --> R["Hybrid retrieval<br/>dense + BM25 → RRF"]
    R --> RR["Cross-encoder<br/>rerank"]
    RR --> G{"Enough<br/>evidence?"}
    G -- no --> X(["Abstain"])
    G -- yes --> L["Grounded<br/>generation"]
    L --> V["Citation<br/>verifier"]
    V --> A
```

</details>

## 🛠️ Tech stack

<div align="center">

### Languages

<p>
  <img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white" alt="Python" />
  <img src="https://img.shields.io/badge/TypeScript-3178C6?style=for-the-badge&logo=typescript&logoColor=white" alt="TypeScript" />
  <img src="https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black" alt="JavaScript" />
  <img src="https://img.shields.io/badge/SQL-336791?style=for-the-badge&logo=postgresql&logoColor=white" alt="SQL" />
  <img src="https://img.shields.io/badge/Bash-4EAA25?style=for-the-badge&logo=gnubash&logoColor=white" alt="Bash" />
</p>

### LLM and agent frameworks

<p>
  <img src="https://img.shields.io/badge/LangChain-1C3C3C?style=for-the-badge&logo=langchain&logoColor=white" alt="LangChain" />
  <img src="https://img.shields.io/badge/LangGraph-1C3C3C?style=for-the-badge&logo=langgraph&logoColor=white" alt="LangGraph" />
  <img src="https://img.shields.io/badge/LlamaIndex-6B46C1?style=for-the-badge" alt="LlamaIndex" />
  <img src="https://img.shields.io/badge/MCP-111111?style=for-the-badge&logo=modelcontextprotocol&logoColor=white" alt="Model Context Protocol" />
  <img src="https://img.shields.io/badge/Hugging_Face-FFD21E?style=for-the-badge&logo=huggingface&logoColor=black" alt="Hugging Face" />
  <img src="https://img.shields.io/badge/Sentence_Transformers-0B7285?style=for-the-badge" alt="Sentence Transformers" />
</p>

### Model providers and local inference

<p>
  <img src="https://img.shields.io/badge/Groq-F55036?style=for-the-badge" alt="Groq" />
  <img src="https://img.shields.io/badge/OpenRouter-6467F2?style=for-the-badge&logo=openrouter&logoColor=white" alt="OpenRouter" />
  <img src="https://img.shields.io/badge/Gemini-8E75B2?style=for-the-badge&logo=googlegemini&logoColor=white" alt="Google Gemini" />
  <img src="https://img.shields.io/badge/OpenAI_API-412991?style=for-the-badge" alt="OpenAI API" />
  <img src="https://img.shields.io/badge/Ollama-111111?style=for-the-badge&logo=ollama&logoColor=white" alt="Ollama" />
</p>

### Retrieval, vector and graph stores

<p>
  <img src="https://img.shields.io/badge/ChromaDB-5B4BDB?style=for-the-badge" alt="ChromaDB" />
  <img src="https://img.shields.io/badge/Pinecone-0B3D2E?style=for-the-badge" alt="Pinecone" />
  <img src="https://img.shields.io/badge/Neo4j-4581C3?style=for-the-badge&logo=neo4j&logoColor=white" alt="Neo4j" />
  <img src="https://img.shields.io/badge/Redis_Stack-DC382D?style=for-the-badge&logo=redis&logoColor=white" alt="Redis Stack" />
  <img src="https://img.shields.io/badge/BM25-37474F?style=for-the-badge" alt="BM25" />
  <img src="https://img.shields.io/badge/BGE_embeddings-0F766E?style=for-the-badge" alt="BGE embeddings" />
  <img src="https://img.shields.io/badge/Cross--encoder_rerankers-7C3AED?style=for-the-badge" alt="Cross-encoder rerankers" />
  <img src="https://img.shields.io/badge/Tavily-1D4ED8?style=for-the-badge" alt="Tavily web search" />
</p>

### Evaluation, testing and observability

<p>
  <img src="https://img.shields.io/badge/Langfuse-0F172A?style=for-the-badge" alt="Langfuse" />
  <img src="https://img.shields.io/badge/Prometheus-E6522C?style=for-the-badge&logo=prometheus&logoColor=white" alt="Prometheus" />
  <img src="https://img.shields.io/badge/Grafana-F46800?style=for-the-badge&logo=grafana&logoColor=white" alt="Grafana" />
  <img src="https://img.shields.io/badge/LLM--as--judge-B45309?style=for-the-badge" alt="LLM-as-judge" />
  <img src="https://img.shields.io/badge/Pytest-0A9EDC?style=for-the-badge&logo=pytest&logoColor=white" alt="Pytest" />
  <img src="https://img.shields.io/badge/Vitest-6E9F18?style=for-the-badge&logo=vitest&logoColor=white" alt="Vitest" />
  <img src="https://img.shields.io/badge/Playwright-2EAD33?style=for-the-badge" alt="Playwright" />
</p>

### Backend and frontend

<p>
  <img src="https://img.shields.io/badge/FastAPI-009688?style=for-the-badge&logo=fastapi&logoColor=white" alt="FastAPI" />
  <img src="https://img.shields.io/badge/PostgreSQL-4169E1?style=for-the-badge&logo=postgresql&logoColor=white" alt="PostgreSQL" />
  <img src="https://img.shields.io/badge/SQLite-003B57?style=for-the-badge&logo=sqlite&logoColor=white" alt="SQLite" />
  <img src="https://img.shields.io/badge/React-20232A?style=for-the-badge&logo=react&logoColor=61DAFB" alt="React" />
  <img src="https://img.shields.io/badge/Vite-646CFF?style=for-the-badge&logo=vite&logoColor=white" alt="Vite" />
  <img src="https://img.shields.io/badge/Streamlit-FF4B4B?style=for-the-badge&logo=streamlit&logoColor=white" alt="Streamlit" />
</p>

### Cloud and DevOps

<p>
  <img src="https://img.shields.io/badge/AWS_EC2_·_SSM-232F3E?style=for-the-badge" alt="AWS EC2 and Systems Manager" />
  <img src="https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white" alt="Docker" />
  <img src="https://img.shields.io/badge/Kubernetes-326CE5?style=for-the-badge&logo=kubernetes&logoColor=white" alt="Kubernetes" />
  <img src="https://img.shields.io/badge/GitHub_Actions-2088FF?style=for-the-badge&logo=githubactions&logoColor=white" alt="GitHub Actions" />
  <img src="https://img.shields.io/badge/Caddy-1F88C0?style=for-the-badge&logo=caddy&logoColor=white" alt="Caddy" />
  <img src="https://img.shields.io/badge/Trivy-1904DA?style=for-the-badge&logo=trivy&logoColor=white" alt="Trivy" />
  <img src="https://img.shields.io/badge/Linux-FCC624?style=for-the-badge&logo=linux&logoColor=black" alt="Linux" />
  <img src="https://img.shields.io/badge/Git-F05032?style=for-the-badge&logo=git&logoColor=white" alt="Git" />
</p>

### Machine learning and computer vision

<p>
  <img src="https://img.shields.io/badge/PyTorch-EE4C2C?style=for-the-badge&logo=pytorch&logoColor=white" alt="PyTorch" />
  <img src="https://img.shields.io/badge/TensorFlow-FF6F00?style=for-the-badge&logo=tensorflow&logoColor=white" alt="TensorFlow" />
  <img src="https://img.shields.io/badge/scikit--learn-F7931E?style=for-the-badge&logo=scikitlearn&logoColor=white" alt="scikit-learn" />
  <img src="https://img.shields.io/badge/NumPy-013243?style=for-the-badge&logo=numpy&logoColor=white" alt="NumPy" />
  <img src="https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=pandas&logoColor=white" alt="Pandas" />
  <img src="https://img.shields.io/badge/OpenCV-5C3EE8?style=for-the-badge&logo=opencv&logoColor=white" alt="OpenCV" />
  <img src="https://img.shields.io/badge/YOLOv5-111F68?style=for-the-badge" alt="YOLOv5" />
</p>

</div>

| Area | What I work with |
| --- | --- |
| **Retrieval** | Hybrid dense + sparse search, reciprocal rank fusion, cross-encoder reranking, query rewriting, semantic caching, knowledge-graph expansion |
| **Generation** | Grounded answers with citations, sufficiency gating and abstention, citation verification by a second model, provider fallback chains, streaming |
| **Agents** | LangGraph state graphs, ReAct, corrective RAG with graders, tool design, MCP |
| **Evaluation** | Golden datasets, recall@k and MRR, calibrated LLM judges, paired bootstrap confidence intervals, sign tests, regression gates in CI |
| **Safety** | Prompt-injection scanning, PII masking, audit logs, rate limiting |
| **Operations** | Deploy on merge with health checks and rollback, SLOs with burn-rate alerts, request tracing, container image scanning |

## 📈 GitHub activity

<div align="center">
  <a href="https://github.com/yashbhosale789">
    <img src="https://github-profile-summary-cards.vercel.app/api/cards/profile-details?username=yashbhosale789&theme=tokyonight" alt="Contribution summary" />
  </a>
</div>

<div align="center">
  <a href="https://github.com/yashbhosale789">
    <img height="180" src="https://github-profile-summary-cards.vercel.app/api/cards/stats?username=yashbhosale789&theme=tokyonight" alt="GitHub statistics" />
    <img height="180" src="https://github-profile-summary-cards.vercel.app/api/cards/repos-per-language?username=yashbhosale789&theme=tokyonight" alt="Repositories per language" />
  </a>
</div>

<div align="center">
  <a href="https://github.com/yashbhosale789">
    <img src="https://streak-stats.demolab.com?user=yashbhosale789&theme=tokyonight&hide_border=true" alt="Contribution streak" />
  </a>
</div>

<div align="center">
  <a href="https://github.com/yashbhosale789?tab=achievements">
    <img src="https://trophy.ryglcloud.net/?username=yashbhosale789&theme=tokyonight&no-frame=true&no-bg=true&rank=SSS,SS,S,AAA,AA,A&column=-1" alt="GitHub trophies" />
  </a>
</div>

<div align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/yashbhosale789/yashbhosale789/output/github-contribution-grid-snake-dark.svg" />
    <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/yashbhosale789/yashbhosale789/output/github-contribution-grid-snake.svg" />
    <img alt="Contribution graph snake animation" src="https://raw.githubusercontent.com/yashbhosale789/yashbhosale789/output/github-contribution-grid-snake.svg" />
  </picture>
</div>

<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:70a5fd,50:1f6feb,100:0d1117&height=110&section=footer" width="100%" alt="" />

<img src="https://komarev.com/ghpvc/?username=yashbhosale789&style=flat&color=70a5fd&label=profile+views" alt="Profile views" />

</div>
