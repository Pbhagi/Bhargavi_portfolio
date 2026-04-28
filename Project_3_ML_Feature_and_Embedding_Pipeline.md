# ML Feature & Embedding Pipeline

> A reference pipeline that turns raw events into model-ready features and embeddings, with offline / online parity, dataset versioning, and full lineage from training to inference.

![Feature Store](https://img.shields.io/badge/Feature%20Store-Feast-blue)
![Vector DB](https://img.shields.io/badge/Vector%20DB-pgvector%20%7C%20Pinecone-purple)
![Compute](https://img.shields.io/badge/Compute-PySpark-orange)
![Versioning](https://img.shields.io/badge/Versioning-DVC%20%7C%20LakeFS-lightgrey)

---

## Why This Project

ML systems break in data, not in code. The fix isn't another notebook — it's treating training data like a production asset: versioned, lineage-tracked, validated, and reproducible. This repo shows that pattern end to end on a small but realistic dataset.

## What It Does

- Turns raw behavioral / textual data into denormalized, model-ready feature tables
- Computes both **batch features** (PySpark on object storage) and **streaming features** (Kafka + Spark Structured Streaming)
- Registers features in a **feature store** (Feast) with offline + online stores
- Generates **text embeddings** and indexes them in a **vector database** (pgvector / Pinecone / Weaviate)
- Versions training datasets with **Delta Lake time travel** and **LakeFS / DVC**
- Tracks **lineage** so any model run can be traced back to exact inputs

## Architecture

```
 Raw events ─▶ Bronze ─▶ Silver (cleaned)
                              │
              ┌───────────────┴──────────────┐
              ▼                              ▼
    Batch feature pipeline          Streaming feature pipeline
       (PySpark on EMR)              (Spark Structured Streaming)
              │                              │
              └────────────┬─────────────────┘
                           ▼
                      Feast (offline + online)
                           │
                           ▼
              ┌────────────┴──────────────┐
              ▼                           ▼
        Training jobs              Online inference / RAG
        (MLflow tracking)          (pgvector / Pinecone)
```

## Highlights

- **Offline / online parity** — same transformation logic for training and serving
- **Point-in-time correctness** when joining features to labels
- **Dataset versioning** so a re-train on the same version reproduces the same model
- **Embedding pipeline** with batched encoding, deduplication, and incremental upserts to the vector DB
- **Quality gates** — schema, freshness, drift, and coverage checks before features are published
- **Lineage** via OpenLineage + MLflow so every model artifact links back to its dataset version

## Tech Stack

`Feast` · `PySpark` · `Spark Structured Streaming` · `Delta Lake` · `LakeFS / DVC` · `pgvector` *(or Pinecone / Weaviate)* · `MLflow` · `OpenLineage` · `Airflow` · `Docker`

## Quick Start

```bash
# spin up local stack: postgres + pgvector + feast + mlflow
docker compose up -d

# materialize features
feast apply
python pipelines/batch_features.py

# generate and index embeddings
python pipelines/embed_and_index.py

# run a sample training job with lineage
python training/train.py --dataset-version v2
```

## What I Learned

- Point-in-time joins matter more than fancy models — leakage destroys both metrics and trust
- Vector databases are easy to populate and hard to keep *fresh*; design the upsert path first
- "Reproducible" really means: same data version + same code version + same feature definitions

## Roadmap

- [ ] Add a small RAG demo that consumes the embedding index
- [ ] Add Tecton-style transformation DSL example
- [ ] Drift dashboards for both features and embeddings

---

<sub>Part of my open data-platform portfolio.</sub>
