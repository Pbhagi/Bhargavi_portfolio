# Modern Analytics Stack Demo

> A complete end-to-end ELT example: ingestion to warehouse to dimensional model to semantic layer to dashboards. Built so any analyst or engineer can clone, run, and extend in under thirty minutes.

![Stack](https://img.shields.io/badge/Stack-Modern%20Data%20Stack-teal)
![Transform](https://img.shields.io/badge/Transform-dbt-orange)
![BI](https://img.shields.io/badge/BI-Looker%20%7C%20Metabase-lightblue)

---

## Why This Project

Most "modern data stack" tutorials stop at "I ran a dbt model." This one goes further: a real semantic layer, conformed dimensions, exposures, dashboards, and the small details (tests, docs, exposures, freshness) that separate a demo from a useful platform.

## What It Does

- Ingests sample SaaS / e-commerce data with a lightweight EL tool (Airbyte / Meltano / Fivetran-style stub)
- Loads raw data into a cloud warehouse (BigQuery / Snowflake / Postgres for local)
- Models data with **dbt** — staging ▶ intermediate ▶ marts
- Implements **dimensional models** (Kimball) and an explicit **semantic layer**
- Publishes **dashboards** in Looker / Metabase that read from the marts
- Documents **exposures** so any model change shows downstream impact

## Architecture

```
   Sources (Postgres / API / SaaS)
            │
            ▼
       Raw schema (warehouse)
            │
            ▼
        dbt staging
            │
            ▼
      dbt intermediate
            │
            ▼
   dbt marts (facts + dims)
            │
            ▼
   Semantic layer (dbt SL / Cube / LookML)
            │
            ▼
       BI dashboards
```

## Highlights

- **Tests on every model** — uniqueness, not-null, referential integrity, accepted values
- **Generated docs** with full lineage and column-level descriptions
- **Exposures** so dashboard owners know when an upstream model changes
- **Macros** for re-usable patterns (audit columns, surrogate keys, conformed dates)
- **CI** that runs `dbt build` against a sandbox dataset on every PR

## Tech Stack

`dbt` · `BigQuery / Snowflake / Postgres` · `Airbyte / Meltano` · `Looker / Metabase / Cube` · `GitHub Actions`

## Project Layout

```
.
├── extract_load/          # EL scripts / Airbyte connectors
├── dbt/
│   ├── models/
│   │   ├── staging/
│   │   ├── intermediate/
│   │   └── marts/
│   ├── tests/
│   ├── macros/
│   └── exposures/
├── dashboards/            # Looker LookML / Metabase JSON
└── .github/workflows/dbt-ci.yml
```

## Quick Start

```bash
# spin up a local Postgres warehouse
docker compose up -d

# load sample data
python extract_load/load_samples.py

# build the warehouse
cd dbt && dbt build

# explore docs + lineage
dbt docs serve
```

## What I Learned

- A small, well-tested mart is worth more than a sprawling collection of "ad hoc" tables
- Naming is the user interface of a data platform — invest in it
- Exposures + tests are the cheapest insurance against angry stakeholders

## Roadmap

- [ ] Add semantic layer queries through dbt SL
- [ ] Add freshness + cost dashboards
- [ ] Add a row-level security example for sensitive marts

---

<sub>Part of my open data-platform portfolio.</sub>
