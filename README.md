# Awesome-RAG-Applications

## Top RAG Applications Ecosystem

**Curated List of SaaS Products & Open-Source GitHub Projects**  
*Focused on Enterprise Knowledge Search, Cited Document Analysis & Self-Hosted RAG Platforms*  
**Last updated: March 2026**

This repository tracks notable **SaaS platforms** and **open-source projects** for **RAG Applications**. These are not frameworks or libraries — they are complete applications that connect to your data sources, build an index, and answer questions with citations, ready to deploy or self-host.

**Examples** include Glean, Onyx, OpenBeam, Coveo, Amazon Kendra, AlphaSense, Hebbia, Verba, RAGFlow, and Kotaemon (the category leaders).

**Open-source emphasis**: This section is heavily expanded with every major active project for self-hosting, permission-aware search, and cited answers — ideal for teams prioritizing data sovereignty, avoiding per-seat enterprise search pricing, and running RAG applications they fully control.

Contributions welcome! Open a PR to add/update entries. Keep descriptions factual and link to official sites.

## Table of Contents
- [SaaS/Hosted Platforms](#saas-hosted-platforms)
- [Open-Source GitHub Projects](#open-source-github-projects)
- [How to Contribute](#how-to-contribute)
- [Disclaimer](#disclaimer)

## SaaS/Hosted Platforms

- **[Glean](https://www.glean.com/)**  
  **The reference enterprise search and knowledge discovery platform** that defined the "AI-powered workplace search" category. Connects to 100+ workplace applications (Slack, Google Drive, Confluence, Jira, Salesforce) to build a unified index. Uses LLM-powered relevance and personalization to surface the right documents, messages, and experts. **Glean proved the digital half at a $7.2B valuation** [citation:2]. **Best for enterprises wanting turnkey search across fragmented SaaS tools** without building connectors themselves.

- **[Coveo](https://www.coveo.com/)**  
  **AI-powered enterprise search and relevance platform** for customer service, workplace, and commerce use cases. Strong connectors for Salesforce, ServiceNow, SharePoint, and legacy systems. **Best for large enterprises** needing unified search across heterogeneous systems with relevance tuning.

- **[Amazon Kendra](https://aws.amazon.com/kendra/)**  
  **AWS-managed intelligent enterprise search** with natural language queries and connectors to S3, SharePoint, Salesforce, and databases. **Best for AWS-native organizations** wanting managed search without infrastructure.

- **[AlphaSense](https://www.alpha-sense.com/)**  
  **AI-powered market intelligence and document search platform** for financial professionals. Indexes SEC filings, earnings calls, broker research, and news. **Best for investment research and competitive intelligence** on professional documents.

- **[Hebbia](https://www.hebbia.com/)**  
  **AI-powered document analysis platform** for financial and legal professionals. Uses LLM reasoning over document collections to answer complex questions with citations. **Best for high-stakes document review** where traceability matters. **OpenGP positions itself as an open-source alternative to Rogo, Hebbia, and BlueFlame** for private equity [citation:5].

- **[Sinequa](https://www.sinequa.com/)**  
  **Enterprise search and intelligence platform** with 200+ connectors, natural language processing, and AI-powered relevance. **Best for regulated industries** requiring on-premise deployment and deep content analytics.

- **[Lucidworks Fusion](https://lucidworks.com/)**  
  **Enterprise search platform built on Apache Solr** with AI-powered relevance, connectors, and a visual query pipeline designer. **Best for organizations wanting Solr's power with enterprise tooling and support**.

- **[Elastic Enterprise Search](https://www.elastic.co/enterprise-search)**  
  **Hosted enterprise search from Elastic** with connectors for content sources, a web crawler, and relevance tuning UI. Integrates with Elasticsearch's vector and hybrid search capabilities. **Best for teams already on the Elastic stack.**

- **[Algolia](https://www.algolia.com/)**  
  **Developer-favorite hosted search API** with instant search, typo tolerance, and relevance out of the box. **Record-based pricing** scales steeply with catalog size. **Best for site search and e-commerce discovery** where fastest time-to-value matters.

## Open-Source GitHub Projects

- **[Onyx](https://github.com/onyx-dot-app/onyx)**  
  **The closest open-source alternative to Glean** — self-hosted enterprise search and AI assistant platform [citation:9]. **40+ app integrations** including Slack, Google Drive, Confluence, Jira, and more [citation:3]. **Document-level permission inheritance** from connected sources — users only see what they have access to [citation:3]. **Fully private deployment** via VPC or on-premises; data never leaves your environment [citation:3]. **Model-agnostic** — supports any model provider or self-hosted LLM [citation:3]. **$10M seed funding** from Khosla Ventures and First Round Capital, trusted by Ramp [citation:3]. **32,000+ GitHub stars**, actively maintained (last commit within hours as of September 2026) [citation:3]. **Best for teams wanting a self-hosted Glean alternative** with permission-aware retrieval and no license line — you own upgrades, scaling, and connector maintenance [citation:9].

- **[OpenBeam](https://github.com/kuluruvineeth/openbeam)**  
  **"Open-source Glean for SaaS and the physical world"** — AGPL licensed, self-hosted [citation:2]. **87 connectors** spanning digital tools (Slack, GitHub, Notion, Linear, Salesforce, Jira, Gmail) and **physical operations** (IoT via Samsara, Verkada, AWS IoT; industrial protocols via MQTT, OPC-UA, BACnet) [citation:2]. **Hybrid semantic + keyword search** with **sub-200ms p99 latency** [citation:2]. **RAG pipeline** with citation and source attribution [citation:2]. **MCP Server** for Claude Code, Cursor, and Codex integration [citation:2]. **Permission-aware** — respects source permissions [citation:2]. **Six pre-built autonomous agents** on Temporal cron schedules with approval gating [citation:2]. **Docker Compose deployment** on your infrastructure [citation:2]. **The only platform bridging SaaS tools and physical operations data in one query** [citation:2]. **Best for organizations needing search across both digital and industrial/IoT systems** — a gap Glean doesn't address.

- **[Verba](https://github.com/weaviate/Verba)**  
  **Weaviate's "Golden RAGtriever"** — a fully aesthetic, open-source RAG web application pre-configured with best practices for chunking, embedding, and retrieval out of the box [citation:6]. **Model support**: OpenAI (GPT-3/4, Ada), Anthropic, Cohere, Groq, Ollama (local models), HuggingFace (local embeddings), VoyageAI, and more [citation:6]. **Data ingestion**: Unstructured.io (PDF, DOCX, etc.), AssemblyAI (audio/video transcription), GitHub, GitLab, Firecrawl (web crawling) [citation:6]. **Deployment**: pip install, Docker Compose, or source build [citation:6]. **Multi-user collaboration is out of scope** — not designed for enterprise multi-tenant deployments [citation:6]. **Best for teams wanting a working RAG application immediately** with sensible defaults and broad model support.

- **[RAGFlow](https://github.com/infiniflow/ragflow)**  
  **The leading open-source RAG engine with deep document understanding** — Apache 2.0 licensed, **133,000+ GitHub stars** [citation:7]. **Layout-aware DeepDoc parsing** using YOLOv8-based layout detection to segment documents before OCR, preserving column/row coordinate mappings for tables and auto-rotating scanned tables [citation:8]. **Template-based chunking** (Law, Manual, Book, Paper, Resume, Table) matches parsing strategy to document semantics [citation:8]. **Hybrid retrieval** (BM25 + dense vector RRF) with **pixel-exact bounding box citations** [citation:8]. **Native integration** with Claude, GPT, Gemini, DeepSeek, Gemma, and Qwen [citation:8]. **Trade-offs**: **high resource requirements** — 16GB+ RAM and GPU recommended for production parsing latency below 2 seconds per page [citation:8]. **Best for legal, financial, healthcare, and technical document Q&A** where table extraction and citation-grade answers matter.

- **[Kotaemon](https://github.com/Cinnamon/kotaemon)**  
  **Local-first RAG UI with visual citations and multi-vector retrieval** — Apache 2.0 licensed [citation:8]. **Multi-vector/parent-child indexing**: small child chunks (100-200 tokens) for semantic mapping linked to larger parent sections (1000-2000 tokens) passed as context [citation:8]. **Visual citation feature** — clicking a citation opens a PDF page viewer with a highlighted bounding box on the text segment [citation:8]. **Gradio UI**, note-centric, supports GraphRAG [citation:8]. **Best for local-first document Q&A** with verifiable citations, though it relies heavily on Ollama and does not manage co-resident VRAM state — can OOM on 12 GB rigs when embedding, reranking, and generation run concurrently [citation:8].

- **[OpenGP](https://github.com/vivan1211/opengp)**  
  **Self-hosted AI intelligence platform for private equity** — AGPL-3.0 licensed, positioned as an open-source alternative to Rogo, Hebbia, and BlueFlame [citation:5]. **Cited AI chat (RAG)** over your data room and portfolio — every figure links to the exact passage [citation:5]. **Data room** with server-side parsing (OCR + tables), chunking, embeddings, and hybrid retrieval (pgvector + full-text + rerank) [citation:5]. **Portfolio analytics** with MOIC/IRR/DPI KPIs [citation:5]. **Model Builder** writes and runs real code in an isolated sandbox [citation:5]. **Multi-tenant with Postgres row-level security** (~96 policies) [citation:5]. **Full Terraform infrastructure** (~77 resources) deployable into your own AWS account [citation:5]. **2,200+ tests** with CI on every PR [citation:5]. **Best for private equity and financial firms** wanting cited document analysis with full data sovereignty.

### Additional Strong Open-Source Options

- **PragmaSearch** — Local-first semantic search engine, open-source Algolia alternative. Hybrid vector + BM25 ranking with typo tolerance and faceting. Built for small-to-mid catalogs (≤50k items), $0 per search, one local index file [citation:4].
- **Meilisearch** — Lightning-fast open-source search engine with hybrid semantic search and agentic retrieval for RAG. 57,000+ GitHub stars, MIT licensed [citation:10].
- **Typesense** — Open-source Algolia alternative with typo tolerance, hybrid search, and vector search. Single binary, no dependencies [citation:11].
- **piragi** — "The best RAG interface yet." Zero-config RAG with built-in vector store, citations, and auto-updates. `pip install piragi` [citation:15].
- **Corpus** — Open-source structured research engine. Upload hundreds of documents, ask dozens of questions, get back a clean spreadsheet in parallel [citation:12].

**Frameworks for building custom systems**: Combine **Onyx** for self-hosted Glean-style enterprise search with permission-aware retrieval across 40+ connectors, **OpenBeam** for search spanning both SaaS tools and physical/IoT operations, **RAGFlow** for vision-native document parsing with pixel-exact citations, **Kotaemon** for local-first visual citations, **Verba** for immediate working RAG with broad model support, and **OpenGP** for private equity-specific cited document analysis — to build a RAG application stack tailored to your data sources, citation requirements, and deployment constraints.

## How to Contribute

1. Fork the repo.
2. Add/edit entries in `README.md` (follow existing format).
3. Include: name, link, 1–2 sentence description, and whether it's SaaS or open-source.
4. Submit PR with a short explanation.

Star the repo if you find it useful!

## Disclaimer

- This is a **community-curated** list — not exhaustive and not an endorsement.
- RAG applications differ significantly in connector breadth, permission handling, and deployment complexity. **Onyx is the closest open-source Glean alternative** with document-level permission inheritance and 40+ connectors — but you own upgrades, scaling, and connector maintenance [citation:9]. **OpenBeam is the only platform bridging SaaS and physical/IoT data** in one query [citation:2]. **RAGFlow has the best document parsing in the OSS RAG space** but requires 16GB+ RAM and GPU for production latency [citation:8]. **Kotaemon can OOM on 12 GB GPUs** when embedding, reranking, and generation run concurrently [citation:8]. **Verba's multi-user collaboration is out of scope** — not designed for enterprise multi-tenant deployments [citation:6]. **OpenGP's infrastructure is Terraform-deployable into your own AWS account** but requires AWS services and ~half a day to set up [citation:5].
- Self-hosted open-source solutions require proper connector maintenance, identity mapping, permission enforcement, and ongoing operations — self-hosting removes the license line but adds an operations line [citation:9].

---

**Made for AI engineers, enterprise search teams, and organizations building grounded document intelligence applications.**
Let's make RAG applications more open, permission-aware, and citation-traceable.
