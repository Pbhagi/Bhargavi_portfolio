<!--
  HOW TO USE THIS FILE
  --------------------
  1. Replace the placeholders YOUR-USERNAME and YOUR-LINKEDIN with your real handles.
  2. If all your project files are inside ONE repo (the GitHub Pages setup),
     leave the project links as ./Project_X_*.md (relative links).
     If each project is its own repo, switch back to the
     https://github.com/YOUR-USERNAME/<repo-name> form.
  3. Paste this entire file as Readme.md (or README.md) and commit.
-->

<h1 align="center">Hi, I'm Bhargavi Reddy P</h1>

<p align="center">
  <em>I build dependable data systems — from raw events to trustworthy datasets that power analytics, ML, and decisions.</em>
</p>

<p align="center">
  <a href="https://www.linkedin.com/in/YOUR-LINKEDIN/"><img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" /></a>
  <a href="mailto:breddyp2321@gmail.com"><img src="https://img.shields.io/badge/Email-D14836?style=for-the-badge&logo=gmail&logoColor=white" /></a>
  <a href="https://github.com/YOUR-USERNAME"><img src="https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white" /></a>
</p>

---

### About Me

I design and operate production-grade batch and streaming data pipelines on the cloud, partner closely with ML and analytics teams to ship trustworthy datasets, and care about the boring parts that keep data systems alive — schema contracts, lineage, idempotency, observability, and cost.

- 4+ years building pipelines on **GCP** and **AWS** across regulated and large-scale consumer domains
- Comfortable across the full stack: ingestion, modeling, semantic layers, BI, and ML feature pipelines
- Strong opinions on data quality, reproducibility, and infrastructure-as-code
- Currently sharpening: streaming systems, vector search, dataset versioning, and developer experience for data platforms

---

### What I'm Good At

**Languages & Query**  Python (PySpark, Pandas, asyncio) · Advanced SQL · Scala · Bash

**Pipelines & Orchestration**  Apache Airflow · dbt · Cloud Composer · Dagster · Prefect · AWS Glue · Azure Data Factory · Apache NiFi · Fivetran

**Streaming & Distributed Compute**  Apache Kafka · Spark Structured Streaming · Apache Beam · Apache Flink · Pub/Sub · Kinesis · Dataproc · EMR · Databricks · Ray

**Storage, Warehouse & Lakehouse**  BigQuery · Snowflake · Redshift · Delta Lake · Apache Iceberg · Apache Hudi · Medallion Architecture · Kimball Dimensional Modeling

**Cloud Platforms**  GCP (BigQuery, Dataflow, Composer, Dataplex, Vertex AI, GCS, Pub/Sub) · AWS (S3, Glue, Redshift, EMR, Lambda, Kinesis, EKS) · Azure (ADLS, ADF, Synapse, Databricks)

**ML Data & Vector Stack**  Feature Stores (Feast, Tecton, Vertex AI Feature Store) · Vector DBs (Pinecone, Weaviate, pgvector, Chroma) · MLflow · DVC · LakeFS

**Quality, Governance & Observability**  Great Expectations · Soda · dbt tests · Monte Carlo · OpenLineage · Data Catalog · RBAC · Column-level Security · HIPAA / GDPR / SOC 2 awareness

**DevOps & IaC**  Docker · Kubernetes (GKE, EKS, AKS) · Terraform · Helm · GitHub Actions · GitLab CI · Jenkins

**BI & Semantic**  Looker (LookML) · Tableau · Power BI · Omni · dbt Semantic Layer · Cube

---

### Experience

#### CVS Health — Data & ML Platform Engineer
*Mar 2025 – Present*

- Architected end-to-end batch and streaming pipelines on GCP (Cloud Dataflow / Apache Beam, Cloud Functions, Cloud Workflows, Cloud Composer) ingesting 3+ TB across 8+ source systems in regulated healthcare data domains
- Designed an enterprise lakehouse on GCS with Dataplex, Data Catalog, and Iceberg-style medallion architecture; partitioning + clustering improved downstream BigQuery query efficiency ~35%
- Built real-time ingestion using Pub/Sub, Dataflow Streaming, Apache Kafka, and Spark Structured Streaming achieving sub-5-second end-to-end latency across 20+ SLA-bound workflows
- Partnered with ML and data science teams to ship training, evaluation, and feature datasets — with dataset versioning (Delta Lake time travel + LakeFS), lineage (OpenLineage), and full reproducibility
- Stood up a feature store on Vertex AI Feature Store and a vector database (pgvector / Pinecone) for embedding storage powering retrieval-augmented search and model evaluation
- Implemented a data quality framework (Great Expectations, dbt tests, Dataplex) with schema validation, drift detection, and anomaly alerting — cutting downstream incidents by ~40%
- Migrated legacy SQL Server / Oracle / SSIS workflows to GCP-native services (Dataflow, Data Fusion, BigQuery, dbt), reducing operational cost ~30%
- Modeled semantic layers in dbt and LookML using Kimball dimensional modeling, enabling self-serve analytics in Looker, Tableau, and Power BI for 50+ stakeholders
- Enforced HIPAA-compliant governance with IAM, BigQuery column-level security, KMS encryption, RBAC, masking, and tokenization
- Deployed pipelines and infra as code (Terraform, Helm, GitHub Actions on GKE) with full CI/CD and test automation across dev/staging/prod
- Built an internal self-serve data portal so ML engineers and analysts can discover and request datasets independently — cutting data request turnaround by ~50%

> **Stack:** GCP (BigQuery, Dataflow, Dataproc, Pub/Sub, Composer, Dataplex, Vertex AI, GKE), Snowflake, Spark, PySpark, Kafka, Flink, dbt, Airflow, Looker, Great Expectations, Monte Carlo, OpenLineage, Pinecone, pgvector, Terraform, Helm, GitHub Actions

#### Meta — Data Engineer, ML & Recommendation Systems
*Aug 2024 – Feb 2025*

- Designed high-throughput batch and streaming pipelines on AWS EMR + Apache Spark and Kafka + Kafka Streams, processing 500B+ daily user interaction events for recommendation and ranking
- Built petabyte-scale feature engineering pipelines using PySpark on EMR and Ray on EKS, transforming raw behavioral and multimodal signals into denormalized, model-ready Delta Lake datasets on S3
- Translated ML model requirements into production training data pipelines, dataset versioning, and evaluation datasets with end-to-end lineage and reproducibility guarantees
- Engineered a Feast-based feature store and embedding pipelines backed by a vector database (Weaviate / pgvector) for similarity search and candidate generation at scale
- Developed reusable Spark ETL frameworks with schema enforcement, schema evolution, CDC, and backfills orchestrated via Dataswarm / Airflow — reducing inconsistencies in recommendation datasets
- Built experimentation pipelines for large-scale A/B testing — CTR, retention, watch-time metrics — managing exposure logging and attribution in Redshift and dbt for reproducible analysis
- Implemented dataset discovery tooling and an internal self-serve catalog used by ML researchers
- Enforced privacy controls around sensitive behavioral and conversational data using access controls, masking, and RBAC aligned with GDPR and internal frameworks

> **Stack:** Spark, PySpark, Ray, Kafka, Kafka Streams, AWS EMR / S3 / EKS, Delta Lake, Redshift, dbt, Airflow, Dataswarm, Feast, Weaviate, pgvector, Python, Docker, Kubernetes, Terraform

#### Accenture — Data Engineer, Cloud Migration & Warehouse Modernization
*Feb 2021 – Jul 2023*

- Built scalable ETL pipelines with AWS Glue, PySpark, and Apache Airflow ingesting patient claims, EHR, lab, and pharmacy data from 10+ sources into AWS Redshift — improving analytics readiness by ~35%
- Led a 3+ TB migration of sensitive data from on-premise Oracle and SQL Server to AWS Redshift; partition / distribution / sort-key tuning improved query performance ~45% for population-health analytics
- Designed dimensional models (star and snowflake) and a Kimball-style warehouse with conformed dimensions, SCD2, and fact tables supporting reimbursement and clinical operations reporting
- Reduced duplicate records by ~40% using Python (Pandas) and SQL deduplication; added dbt tests + Great Expectations for schema validation and quality
- Automated batch and incremental loads with Airflow + Bash on Linux, replacing manual refresh and cutting job runtime ~28%
- Built CI/CD with Git, Bitbucket, Jenkins, and Docker; integrated AWS CloudWatch for observability and alerting
- Operated in Agile/Scrum/Kanban using JIRA — defect management, status reporting, risk/issue tracking, business stakeholder reviews and sign-off
- Mentored 4+ junior engineers on SQL optimization, distributed systems, and pipeline best practices; authored runbooks, design docs, and Confluence knowledge bases

> **Stack:** AWS (Glue, Redshift, S3, CloudWatch, IAM, EC2, EKS), PySpark, Airflow, Python, SQL, Oracle, SQL Server, PostgreSQL, dbt, Great Expectations, Git, Bitbucket, Docker, Kubernetes, Jenkins, JIRA, Confluence

---

### Featured Projects

| Project | What It Demonstrates | Stack |
| --- | --- | --- |
| [Real-Time Streaming Pipeline](./Project_1_Real-time_streaming_pipeline.md) | Sub-5s end-to-end ingestion, exactly-once semantics, schema evolution | Kafka · Spark Structured Streaming · Delta Lake |
| [Cloud Lakehouse with Medallion Architecture](./Project_2_cloud_lakehouse_with_medallion_architecture.md) | Bronze/Silver/Gold layered lakehouse, partitioning & clustering, dbt models | BigQuery / Snowflake · dbt · Airflow · Iceberg |
| [ML Feature & Embedding Pipeline](./Project_3_ML_Feature_and_Embedding_Pipeline.md) | Offline + online feature parity, embedding generation, vector search | Feast · pgvector · PySpark · Airflow |
| [Data Quality & Contract Framework](./Project_4_Data_Quality_and_Contract_Framework.md) | Schema validation, drift detection, alerting, CI integration | Great Expectations · dbt tests · OpenLineage · GitHub Actions |
| [Modern Analytics Stack Demo](./Project_5_Modern_Analytics_Stack_Demo.md) | End-to-end ELT, dimensional modeling, semantic layer, dashboards | dbt · BigQuery · Looker / Metabase |
| [Infra-as-Code Data Platform](./Project_6_Infrastructure_as_Code_Data_Platform.md) | Reproducible cloud data infra with CI/CD on Kubernetes | Terraform · Helm · GKE · GitHub Actions |

> Each project file has its own architecture, setup steps, and a short "what I learned" note.

---

### How I Work

- **Reliability first** — pipelines should be idempotent, observable, and recoverable; loud when wrong, quiet when right.
- **Contracts over surprises** — schemas, expectations, and SLAs are part of the deliverable, not afterthoughts.
- **Reproducibility** — any model run, any dashboard number, any insight should be traceable to the exact data that produced it.
- **Cost-aware** — partitioning, clustering, query shape, and compute right-sizing are part of every design.
- **Stakeholder fluency** — comfortable in both engineering standups and business reviews; I translate between the two.

---

### Currently Exploring

- Streaming-native lakehouse patterns with Iceberg + Flink
- Retrieval-augmented systems and vector indexing strategies
- Data contracts, semantic-layer-as-code, and self-serve data platforms
- Observability for ML data pipelines (lineage + freshness + drift in one pane)

---

### Education

**Master of Science, Computer Engineering** — University of Bridgeport, USA *(Sep 2023 – May 2025, GPA 3.3 / 4.0)*

Coursework: Cloud Computing, Deep Learning, Reinforcement Learning, Cryptography, Cybersecurity, Data & Computer Communication, Python for Data Science.

### Certifications

- Google Cloud **Professional Data Engineer**
- Snowflake **SnowPro Core**
- AWS **Certified Data Analytics – Specialty** *(in progress)*

---

### Let's Connect

Open to collaborating on open-source data tooling, mentoring early-career engineers, and roles where I can build platforms that other teams want to use.

- LinkedIn: <https://www.linkedin.com/in/YOUR-LINKEDIN/>
- Email: breddyp2321@gmail.com

<sub>Thanks for stopping by. If you found something useful, a star helps more than you'd think.</sub>
