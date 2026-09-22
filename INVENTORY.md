# Presentation Inventory

Inventory of four VAST Data presentation assets, compiled 2026-09-22 by direct
extraction of each file (PDF page text + embedded-image counts via `pypdf`,
slide/shape/notes tree via `python-pptx`, DOM/CSS/JS analysis of the HTML).

## 1. Summary

| # | Asset | Format | Size | Units | Author (file metadata) | File date | Aspect | Speaker notes |
|---|-------|--------|------|-------|------------------------|-----------|--------|----------------|
| A | `2025_VAST_Data_AI_Factory_Basics.pdf` | PDF (PowerPoint export) | 13.2 MB | 47 pages | Greg Mead | 2026-05-15 | 11 × 8.5 in (4:3-ish, letter landscape) | none (PDF) |
| B | `ai-factory.v6.html` | Single-file interactive HTML app | 157 KB | 13 views / 31 charts | — (no metadata) | — | responsive, desktop-first | n/a |
| C | `Copy_-_VAST__AIOS_Kafka.pptx` | PowerPoint | 7.2 MB | 67 slides (1 hidden) | Allen Djal (created 2024-02-08) | — | 13.33 × 7.5 in (16:9) | 31 of 67 slides |
| D | `Copy_-_VAST__AIOS_Kafka.pdf` | PDF (export of C) | 2.9 MB | 66 pages | Allen Djal | 2026-04-21 | 13.33 × 7.5 in (16:9) | none (PDF) |

**Three distinct works, four files:** C and D are the same deck (D is a PDF
export of C, minus C's one hidden slide). A and B are independent assets.

**Coverage at a glance**

- **A — AI Factory Basics:** enablement/education deck. AI fundamentals (GPUs,
  training, fine-tuning, agents, RAG, vectors, KV cache) → AI Factory
  definitions → market/pain points → VAST + NVIDIA positioning.
- **B — AI Factory dashboard demo:** a clickable, animated *product
  demonstration* (not slides) of a life-sciences AI factory running on VAST,
  with simulated live telemetry.
- **C/D — VAST AIOS Kafka / Event Broker:** technical deck. Events primer →
  DASE architecture → Kafka concepts (topics, partitions, pub/sub, consumer
  groups) → VAST Event Broker implementation and claims.

---

## 2. Asset A — `2025_VAST_Data_AI_Factory_Basics.pdf`

**"The Basics — Enterprise AI Fundamentals"**

| Property | Value |
|---|---|
| Embedded PDF title | `2025 VAST Data_AI Factory Basics_v7 (3)` |
| Author / Creator / Producer | Greg Mead / PowerPoint / macOS 15.7.4 Quartz PDFContext |
| Created = modified | 2026-05-15 14:36:50 UTC |
| Pages | 47 |
| Page size | 792 × 612 pt (11 × 8.5 in) |
| Footer | `VAST Data 2026 © All rights reserved` + slide number on most pages |
| Graphics | Image-heavy: 62 embedded images on p2, 56 on p47, 53 on p40, 50 on p15, 43 on p35–38 (built-up diagrams) |

### Structure

**Part 1 — AI fundamentals (pp. 1–14)**

| p | Title |
|---|---|
| 1 | The Basics — Enterprise AI Fundamentals (cover) |
| 2 | Changing Requirements: CPUs to GPUs — parallel compute needs parallel storage; what is CUDA |
| 3 | Parallel Compute Changes Storage Access — CPU vs GPU access-pattern table (7 rows, ends on "GPU starvation") |
| 4 | Models: The Brains of AI — what they do / types / how they're made |
| 5 | Checkpoints Keep Training on Track — asynchronous checkpoints |
| 6 | Large Model Training (diagram only) |
| 7 | Training and Inference — plus the deck's "token" definition |
| 8 | Fine Tuning — optimize models for your business |
| 9 | Fine Tuning – How it's Evolved — full fine-tune vs LoRA (175B params vs 17M adapter) |
| 10 | Fine Tuning vs Training — 6-row comparison table |
| 11 | Agents: What are they? — LLM / Profile / Memory / Tools / Feedback |
| 12 | OpenClaw Example — personal assistant agent (SOUL.md, AGENTS.md, USER.md, MEMORY.md, SKILLS.md; "Claude Opus 4.6" as the reasoning LLM) |
| 13 | Agents: What do they do? — Observe, Plan, Act |
| 14 | OpenClaw Example — Observe, Plan, Act walkthrough (prospect follow-up email) |

**Part 2 — AI Factory definitions (pp. 15–19)**

| p | Title |
|---|---|
| 15 | AI is a 5 Layer Cake — Energy / Chips / Infrastructure / Model / Applications |
| 16 | What is an AI Factory? — NVIDIA's glossary definition |
| 17 | NVIDIA AI Enterprise stack diagram — Agentic AI & Physical AI use cases over NeMo, Run:ai, Omniverse, certified systems/networking/storage |
| 18 | What is an AI Data Platform? — NVIDIA's definition |
| 19 | AI Factory vs AI Data Platform — Different Scopes (6-row comparison) |

**Part 3 — Pipelines, RAG, vectors, context (pp. 20–31)**

| p | Title |
|---|---|
| 20 | What is a pipeline? — triggers and functions |
| 21 | What is a RAG? — 5-step flow, with/without RAG |
| 22 | How does embedding work? — Extract / Prepare / Chunk / Enrich / Load |
| 23 | How does retrieval work? — Embed / Search / Return / Re-Rank / Assemble |
| 24 | What is a vector? — dimensions vs speed vs accuracy table |
| 25 | How does Similarity Search work? — nearest-neighbour search, vector DB |
| 26 | How does AI find the right vectors? — brute force vs ANN (HNSW / IVF / PQ); "Hint – DASE enables something different" |
| 27 | What is context? — training vs context; prefill/decode workers, KV cache |
| 28 | What is KV Cache? — benefits, challenges, NVIDIA Dynamo as solution |
| 29 | KV cache tiering G1–G4 — GPU HBM → DRAM → local SSD → shared object/file, latency vs efficiency vs cost |
| 30 | Introducing NVIDIA Context Memory Storage (CMX) — claims 5× higher tokens/sec; BlueField-4, Spectrum-X, DOCA, NIXL, Dynamo |
| 31 | CMX / Dynamo architecture diagram — Rubin compute, Dynamo Grove, KV$ tiering across racks |

**Part 4 — Market, pain points, VAST positioning (pp. 32–47)**

| p | Title |
|---|---|
| 32 | AI Data Sources — The Fuel (5-row table: sensors, existing corpora, SaaS apps, structured/real-time, streams) |
| 33 | Key Players in Enterprise AI — "The Pitch / The Reality" for clouds, data platforms, HPC storage, vector DBs, infrastructure platforms, enterprise storage |
| 34 | AI Factory Pain Points — fragmentation → complexity → security/visibility loss |
| 35 | AI Factory Pain Points — fragmented-stack diagram with per-component failure callouts |
| 36 | …same diagram: "Data moves, everywhere" |
| 37 | …same diagram: "Different access controls, everywhere" |
| 38 | …same diagram: "Especially here" |
| 39 | The Vector Challenge — sharding, memory-bound, slow updates |
| 40 | VAST Value: DASE + AI OS — DataStore / DataBase / DataEngine layers |
| 41 | Architecture: DASE Overview — 4 vector scalability claims (space, insert, search, ACL atomicity) |
| 42 | VAST Event Broker — streaming, analytics & AI in one platform (**overlaps C/D slide 59**) |
| 43 | VAST InsightEngine — unified engine to ingest and contextualize unstructured data |
| 44 | VAST InsightEngine — unified data & vector access policies (element store / ACL store) |
| 45 | VAST & NVIDIA: Collaborating At Every Level Of The Stack |
| 46 | CMX Architecture with VAST (marked "VAST Data * GTC 2026") |
| 47 | VAST Data Event Triggers and Runtime — end-state architecture, MCP-compatible tools |

### Notes on A

- Filename and embedded title say **2025**, but the content is **2026-vintage**:
  2026 copyright footers, "GTC 2026", NVIDIA Rubin / BlueField-4 / CMX, and
  Claude Opus 4.6. The `2025_` prefix is stale.
- Version string in the metadata is `v7 (3)` — a working copy, not a clean release name.
- Pages 35–38 are a four-step animation build of one diagram; pages 54–56 of
  asset C/D do the same. Any merged deck should collapse these.
- Pages 5, 6, 29, 30, 31, 39, 46 carry no copyright footer (inconsistent with the rest).

---

## 3. Asset B — `ai-factory.v6.html`

**"AI Factory on VAST — GPU-scale AI production"** (page `<title>`) /
on-screen H1: *"Life-Sciences AI Factory — from FAIR data to discovery, at GPU scale"*

This is **not a slide deck**. It is a single-file, self-contained interactive
web application that simulates a running AI factory console — the sort of thing
used as a live demo rather than presented page by page.

| Property | Value |
|---|---|
| Size / lines | 160,363 bytes, 1,320 lines |
| External dependencies | **none** — 0 `<script src>`, 0 `<link href>`, 0 `<img>`, 0 `data:` URIs |
| Implementation | 1 inline `<style>`, 1 inline `<script>`, vanilla JS (no framework or chart library) |
| Structure | 13 `<section class="view">` tabpanels, 12 `<h2>`, 53 `<h3>`, 806 `<div>` |
| Visuals | 31 `<canvas>` charts (hand-drawn), 26 inline `<svg>`, 13 `<table>`, 18 interactive `<button>` |
| Theming | CSS custom properties (`--bg`, `--panel`, `--ink`, `--green`, `--amber`, …); dark theme only — no `prefers-color-scheme` light variant |
| A11y / motion | 17 `aria-*` attributes, `role="tabpanel"` on every view, honours `prefers-reduced-motion` |
| Responsive | 10 `@media` breakpoints, collapsible left rail (`--rail-w`) |
| Data | **Simulated** — labelled "simulated demonstration data" in the subhead |

### Header chrome

`VAST AI FACTORY v6` · cluster `factory-prod-01` · ✓ Online ·
`1,024 GPUs · 8.4 PB all-flash · GPUDirect` · live UTC clock ·
`2 Alarms / 1 critical`

### The 13 views

| # | View (`id`) | Contents |
|---|---|---|
| 1 | Factory Overview (`view-overview`) | KPIs (tokens/sec, models in production, GPU utilisation, cost/1M tokens, revenue, jobs in flight); "Needs attention" rows that deep-link to other views; GPU allocation donut; live throughput; token throughput; top inference endpoints; rolling factory event feed |
| 2 | GPU Fleet (`view-gpu`) | GPUs online, utilisation, GPUDirect read, power draw, avg temp, XID errors 24h; live utilisation/power/bandwidth charts; fleet health; per-node table |
| 3 | Data Foundation (`view-data`) | Capacity used, data reduction, read bandwidth, datasets, checkpoints, embeddings; ingest/bandwidth/flash charts; "The platform"; datasets table |
| 4 | Model Pipeline (`view-pipeline`) | Live fine-tune run (`esm2-3b` → target-affinity predictor) with loss curve; training-runs table; **"Run pipeline"** action |
| 5 | Inference & Serving (`view-inference`) | Endpoints, tokens/sec, p95 TTFT, KV cache util, requests/sec, $/1M tokens; served-token chart; endpoints table |
| 6 | Tenants (`view-tenants`) | Multi-tenant by construction: GPU allocation by tenant, per-tenant isolation, top chargeback, tenants table; toggle *by tenant / by model* |
| 7 | Tokenomics (`view-tokenomics`) | Three switchable models — **serving economics / training economics / model ROI**: cost breakdown, efficiency, spend vs budget, cost vs chargeback, cost by run, "Why it's cheaper here", break-even (training cost vs cumulative chargeback), model ROI (median payback, best ROI, underwater) |
| 8 | Autonomous Lab (`view-lab`) | Self-driving drug discovery: closed-loop campaign, binding-affinity (pIC50) objective, best candidate, campaign log; **"Run campaign" / "Reset"** actions |
| 9 | Collaborative Cleanrooms (`view-cleanroom`) | Cleanrooms list, governed datasets, raw rows egressed, analyses run; **"Run analysis"** (query executes inside the bubble) |
| 10 | Telemetry (`view-telemetry`) | "One substrate for every signal": pipeline, signal throughput, spans/metrics/logs per sec, retention, Trino query p95, stores collapsed; **"Ask the estate" agent diagnosis** with 4 canned investigations (slow inference, failed training job, cost spike, request queuing) |
| 11 | Model Registry (`view-registry`) | Models table + model-card drill-down |
| 12 | GenAI Apps (`view-apps`) | Anatomy of an app on the factory; `agent_sessions`; apps in production, DAUs, tokens/day, spend/day |
| 13 | Self-service (`view-selfservice`) | Provision governed AI services in minutes: service catalogue (project workspace, S3 bucket, VAST DataBase + vectors, Event Broker stream, inference endpoint, AgentEngine agent, RAG app, fine-tune job, collaborative cleanroom); **"Provision & add to chargeback"** |

### Demo dataset

- **Models:** `esm2-3b`, `fold-xl`, `molgen-7b`, `dock-scorer`, `research-copilot`, `path-vision`, `clinical-8b`, `ab-designer`
- **Tenants / cleanrooms:** Population Cohort consortium, Oncology R&D × Clinical Genomics, Vaccines R&D × Imaging cryo-EM, Regulatory sandbox
- **Scripted incidents:** node `dgx-07` — 2 GPUs off the bus (XID 79); fine-tune `ft-2214` loss plateau (`llama-3-70b`, 3 epochs flat); endpoint `llama-70b-chat` p95 latency rising (autoscale +2 replicas)

### Notes on B

- Fully portable: opens from a local file with no network access, nothing to install.
- Named `v6`, and the UI badge agrees (`VAST AI FACTORY v6`) — earlier versions are not in this set.
- Minor defect: four `<h3>` headings leak JS template source into the static
  markup (`'+cr.name+'`, `'+m.name+'`, `'+a.n+'`, `'+s.name+'`). These are
  clones/templates filled at runtime, so they are only visible to a static
  reader, not to the user.

---

## 4. Assets C & D — `Copy_-_VAST__AIOS_Kafka` (.pptx and .pdf)

**"From Stream to Action: Simplifying Real-Time Data Analysis and Operational AI"**
— presenter credited on the cover: **Suyash Ramineni, VAST Data**

| Property | C — PPTX | D — PDF |
|---|---|---|
| Size | 7.2 MB | 2.9 MB |
| Units | 67 slides (**slide 22 hidden**) | 66 pages |
| Slide size | 13.33 × 7.5 in (16:9) | 959.76 × 540 pt (same 16:9) |
| Metadata author | Allen Djal (created 2024-02-08 16:00:48; no modified date, revision 0, empty title) | Allen Djal, created & modified 2026-04-21 14:50:17 UTC |
| Masters / layouts | 2 masters, 8 layouts (`1_Cover`, `Blank_Solid_Dark`, `Single Content Dark`, `OBJECT`, `Column Dark`, `1_Picture Dark`, …) — dark theme | — |
| Media | 36 files (34 PNG, 2 JPG), 6.7 MB total | images embedded per page |
| Charts / tables | 0 native charts, 0 native tables (all visuals are images/shapes) | — |
| Speaker notes | **31 of 67 slides**, several verbatim transcripts (up to ~1.1 K chars) | none |

### C ↔ D mapping

D is a straight PDF export of C with the hidden slide dropped:

- PPTX 1–21 → PDF 1–21
- **PPTX 22 — "The VAST Data Element Store" — hidden, absent from the PDF**
- PPTX 23–67 → PDF 22–66

Because PowerPoint still counts the hidden slide, the *printed footer numbers*
in the PDF run one ahead of the actual page from page 22 onward (PDF page 22
shows footer "23", the last page shows "67" on page 66). Cosmetic, but visible
to an audience.

### Structure (PPTX numbering)

| Slides | Section | Contents |
|---|---|---|
| 1 | Cover | Title + presenter (Suyash Ramineni) |
| 2 | Platform intro | "The Data Platform For The AI Era" — eliminate tiering bottlenecks/silos, structured + unstructured, edge-to-cloud, AI Operating System |
| 3 | Problem framing | "Data Management Has Been Complex for 20 Years" — ETL between transactions / data lake / warehouse / event streams, each with its own trade-off |
| 4–16 | **"EVENTS" build** | Near-textless full-bleed animation sequence: EVENTS → human-generated events (purchase, stock movement, web click, slide 7) → machine-generated events (IoT, networking, apps/microservices, slide 8) → "EVENTS are EVERYWHERE" (9) → "EVENTS are POWERFUL" (10) → K/V build (11–16) |
| 17–22 | DASE architecture | "The architecture of the future" — 20 years after Google (17); challenges of shared-nothing (18); introducing DASE (19); asymmetric clusters, no migrations (20); the VAST DataStore multi-protocol structure (21); **the Element Store (22 — hidden)** |
| 23–31 | Log build | Near-textless build of the immutable log / K-V concept |
| 32 | Immutable Event Log | Events are appended at the end of the log |
| 33–34 | Topics | "TOPICS"; topics are similar in concept to tables in a database (Clicks / Orders / Customers) |
| 35–36 | Partitions | "PARTITIONS"; messages strictly ordered within a partition (Clicks p0/p1/p2) |
| 37–45 | Pub/Sub | "PUB / SUB"; producing data (37–38, round-robin across 4 partitions); sequential-only consumption (40); consumers hold their own offset — 1, 2, then 3 consumers (41–43); multiple consumers (44); grouped consumers (45) |
| 46–51 | Kafka → VAST | Why a Kafka-compliant Event Broker (46–47); what stream processing is used for (48); traditional Apache Kafka architecture — shared-nothing, 3 replicas, page cache, HDD-era design (49); transaction-log implementation, commit/abort markers (50); **VAST Event Broker with Kafka-compliant APIs** — topics/partitions as VAST DataBase tables, VAST DB transactions (no markers needed), bucket = virtual broker cluster, VIP-based partition leaders (51) |
| 52–57 | Database foundation | "TOPICS are TABLES" (52); legacy architectures create compromises — rows-vs-columns, partitioning, east-west traffic (53); breaking the rows/columns trade-off — 7 M batched inserts/sec per server, >20× faster than Parquet for selective ops (54); NVMe-optimized row→column structure, SCM write buffer → 98% low-cost flash (55–56, repeated build); use case: big data analytics with Arrow / S3A / global namespace (57) |
| 58–65 | VAST Event Broker | Today's event streaming is broken (58); introducing the VAST Event Broker — 4 value props (59); world's fastest Kafka-compatible performance: **10× faster than Kafka, up to 1 M events/sec per CNode** (60); from topics to tables (61); simplified by design — no separate Kafka clusters or ZooKeeper (62); deploy in minutes via VAST Management System (63); monitor everything, configure nothing (64); built on DASE (65) |
| 66–67 | Close | "Questions?"; "Thank you" (footer still reads "VAST Data 2024 Overview") |

### Notes on C/D

- **The PPTX is the only source of narration.** 31 slides carry notes, and
  several are literal spoken transcripts (e.g. slide 3 on database-management
  trade-offs, slide 49 on Parquet file/partition sizing, slide 59 on Event
  Broker benefits). None of this survives in the PDF.
- Roughly **28 of 67 slides are near-textless animation builds** (4–16, 23–31,
  33, 35, 37, and the repeated 54–56). In the PDF these become pages carrying
  little more than a number, which makes the PDF a poor read-alone artifact.
- Both files are named `Copy - …`, and the PPTX has an empty title and revision 0
  — a downloaded copy, not a canonical master.
- Stale branding: slide/page footers say "2025 VAST Data Overview" throughout
  and the final slide says "VAST Data 2024 Overview", while the PDF was
  exported 2026-04-21.
- The PPTX core-properties creation date (2024-02-08) long predates the content,
  another artifact of the copy.

---

## 5. Cross-asset overlap and inconsistencies

**Shared content**

| Topic | A | B | C/D |
|---|---|---|---|
| DASE architecture | pp. 40–41 | implied throughout | slides 17–22, 65 |
| VAST Event Broker | p. 42 | Event Broker stream in self-service catalogue | slides 51, 58–65 |
| Topics as DataBase tables | p. 42 | — | slides 33–34, 51, 52, 61 |
| DataStore / DataBase / DataEngine layering | pp. 40, 45 | Data Foundation view | slides 2, 21 |
| InsightEngine / embeddings + vectors | pp. 43–44 | Data Foundation (embeddings), AgentEngine in catalogue | — |
| Vectors / RAG / KV cache | pp. 21–31 | Inference view (KV cache util), RAG app in catalogue | — |
| Kafka mechanics (partitions, offsets, consumer groups) | — | — | slides 32–45 |
| Tokenomics / chargeback / multi-tenancy | — | views 6–7 | — |

**Asset A page 42 and asset C/D slide 59 are the same slide with different numbers:**

| Claim | A p. 42 | C/D slide 59 (PDF p. 58) |
|---|---|---|
| Throughput | up to 1 M events/sec per CNode | up to 1 M events/sec per CNode |
| Latency | "with **neae zero** latency" (typo for *near zero*) | "with **sub-4ms** latency" |

Two different latency claims for the same product on the same slide, and a typo
in A. Pick one number and fix the typo before either deck is reused.

**Other things worth fixing**

1. `2025_VAST_Data_AI_Factory_Basics.pdf` — rename; the content is 2026.
2. C/D footers — "2025 VAST Data Overview" and one "VAST Data 2024 Overview"
   on a 2026 deck.
3. C's hidden slide 22 — decide whether the Element Store slide belongs in the
   flow; leaving it hidden also mis-numbers every later footer in the PDF export.
4. A has no source `.pptx` in this set, and B has no source project — only the
   rendered PDF and the built HTML. C is the only asset delivered with an
   editable source *and* speaker notes.
5. B's four template-literal `<h3>` headings (`'+m.name+'` etc.) are harmless
   at runtime but will confuse anyone reading or diffing the source.

## 6. Gaps in the set

- **No editable source for A** (PDF only) — edits require the original PowerPoint.
- **No speaker notes for A or B** — only C carries narration.
- **No customer-facing one-pager or summary deck** — A is an internal-style
  primer (47 pages), C/D is a deep technical talk (67 slides), B is a live demo.
  None is a short executive pitch.
