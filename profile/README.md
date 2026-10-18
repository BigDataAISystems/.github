# Big Data & AI Systems

**Research • Engineering • Open Source**

Big Data & AI Systems is a research and open-source project organization focused on the intersection of **Big Data, distributed data processing, cloud computing, and AI-powered data systems**.

The organization brings together practical engineering, research-oriented experimentation, and educational projects involving scalable data platforms and modern AI technologies.

## Research & Project Areas

### Big Data & Distributed Systems

Scalable data processing, Apache Spark, distributed analytics, data engineering, and large-scale data management.

### AI-Powered Data Systems

Scalable AI applications that integrate large language models (LLMs), Retrieval-Augmented Generation (RAG), embeddings, vector search, and large-scale data processing.

### Cloud Computing & Optimization

Cloud data management, resource allocation, data placement, workflow scheduling, and optimization of data-intensive applications.

### Intelligent Data Centers

Data-driven and AI-assisted approaches to workload scheduling, resource management, energy efficiency, GPU/thermal analytics, and data-center optimization.

---

## Active Projects

### 🔹 Scalable RAG with Apache Spark

A research-oriented project investigating **Retrieval-Augmented Generation, retrieval quality, corpus scalability, and distributed AI processing** over increasingly large document collections.

The project has evolved from local semantic retrieval and RAG evaluation to **MS MARCO scalability experiments, Apache Spark embedding pipelines, and a reproducible framework for future multi-worker cloud experiments**.

**Current progress:**

- ✅ **V1 — Semantic Retrieval**
  - SciFact corpus
  - Sentence Transformer embeddings
  - FAISS semantic vector search
  - retrieval evaluation

- ✅ **V2 — Local RAG**
  - retrieved-context construction
  - grounded LLM prompting
  - source citations
  - RAG experiment logging

- ✅ **V3 — RAG Evaluation & Top-K Experiments**
  - Recall@K and retrieval-depth analysis
  - groundedness evaluation
  - citation faithfulness and validity
  - stratified Top-K experiments
  - generation-latency analysis

- ✅ **V4 — MS MARCO & Single-Machine Scalability**
  - controlled nested corpora from **1K to 250K documents**
  - 300 fixed evaluation queries
  - embedding-time and memory scaling
  - FAISS index-size and retrieval-latency measurements
  - Recall@5 scaling
  - **250K embedding time: approximately 2.97 hours**
  - identified document embedding as the dominant preprocessing bottleneck

- ✅ **V5 — Apache Spark Local Parallelism**
  - PySpark / Apache Spark embedding pipelines
  - Sentence Transformers inside Spark workers
  - controlled Spark partition and PyTorch-thread experiments
  - Spark-native corpus ingestion
  - demonstrated that increasing local Spark parallelism does not create additional physical compute resources

- ✅ **V6 — Distributed Experiment Framework**
  - configuration-driven Spark experiments
  - experiment and environment provenance
  - expected-document-count safeguards
  - benchmark and materialization modes
  - formal Parquet embedding artifact contract
  - independent artifact validation
  - positive and deliberate-corruption validation tests
  - experiment-integrity analysis
  - strong-scaling analysis framework
  - explicit distinction between **Spark partitions and physical workers**

- ⏳ **V7 — GCP Multi-Worker Spark Scaling**
  - genuine multi-worker cloud execution
  - **1 → 2 → 4 worker strong-scaling experiments**
  - 25K distributed validation
  - 100K primary strong-scaling benchmark
  - 250K large-workload validation
  - speedup and parallel-efficiency analysis
  - distributed Parquet materialization
  - cloud cost/performance analysis

**Selected results:**

- V3 showed that increasing retrieval depth improves evidence availability but does not necessarily improve groundedness or overall RAG quality.
- V4 measured Recall@5 decreasing from **0.9967 at 1K documents to 0.8833 at 250K documents** as the retrieval search space increased.
- V4 required approximately **2.97 hours to embed 250K MS MARCO passages**, identifying embedding as the dominant preprocessing bottleneck.
- V5 showed that additional local Spark tasks do **not** provide meaningful acceleration when they share the same physical compute resources.
- V6 established a reproducible distributed experiment framework with configuration provenance, correctness safeguards, artifact validation, and future strong-scaling analysis.

A central methodological principle established in V6 is:

> **Spark partitions are not equivalent to physical workers.**

True distributed speedup will therefore be measured only when additional workers correspond to genuinely additional compute resources.

**Repository:** [BigDataAISystems/scalable-rag-spark](https://github.com/BigDataAISystems/scalable-rag-spark)

---

### 🔹 Big Data Vector Search

Experiments with large-scale embedding generation, vector indexing, semantic retrieval, and vector-search performance.

### 🔹 LLM-Powered Big Data Analytics

Natural-language interfaces and LLM-assisted analytics over large-scale structured and unstructured data.

### 🔹 Streaming Data + AI

Exploration of real-time data processing and AI-assisted analytics using technologies such as Spark Structured Streaming.

---

## Featured Projects

### Snowflake Retail Analytics Pipeline

An end-to-end data engineering and analytics pipeline using **Snowflake, SQL, and Python**, including data ingestion, transformation, validation, analytics, and visualization.

> Additional documentation and repository improvements are in progress.

---

## Collaboration

We welcome opportunities to connect projects with research, education, and real-world applications.

### Master's Students

Research-oriented projects in Big Data, distributed systems, cloud computing, data engineering, and AI-powered data systems.

### Faculty & Researchers

Collaborative research involving scalable data systems, AI-powered data infrastructure, cloud computing, optimization, and intelligent computing systems.

### Industry Partners

Applied research, student-industry projects, datasets and case studies, prototypes, and collaborations involving large-scale data and AI systems.

---

## Technologies

`Apache Spark` · `PySpark` · `Python` · `SQL` · `Snowflake` · `Google Cloud` · `Databricks` · `Cloud Computing` · `Vector Search` · `FAISS` · `RAG` · `LLMs`

---

## About

Big Data & AI Systems is led by **Mahdi Ebrahimi, Ph.D.**, Associate Professor of Computer Science at California State University, Northridge (CSUN).

His research focuses on **Big Data, large-scale data systems, cloud computing, and optimization**, with current interests at the intersection of **Big Data and Artificial Intelligence**, including scalable AI-powered data systems.

---

## Links

- **Academic Website:** https://mebrahimii.github.io/
- **GitHub Organization:** https://github.com/BigDataAISystems
- **Scalable RAG Project:** https://github.com/BigDataAISystems/scalable-rag-spark
- **CSUN Computer Science:** https://www.csun.edu/engineering-computer-science/computer-science

---

*Building scalable data systems and exploring the next generation of AI-powered data infrastructure.*